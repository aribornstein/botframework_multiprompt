# Botframework MultiPrompt

The existing botframework prompts allow you to choose only a specific input type, whether its a text, attachment or anything else.
To select a prompt dynamically you had to use 'choice prompt' prior to the actual desired prompt, which negatively affects the user experience.
This custom prompt allows the user to enter text OR a single attachment dynamically.

## Usage example
  ```
    var bot = new builder.UniversalBot((connector));

    builder.Prompts.multiPrompt = multiPrompt.multiPromptsLauncher;
    bot.dialog('multiPrompt', multiPrompt.multiPrompt);

    // then just ask for input
    builder.Prompts.multiPrompt(session, "Please upload an image or type your message");
  ```