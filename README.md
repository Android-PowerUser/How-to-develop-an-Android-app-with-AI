## How to develop an Android app with AI

# App Development with AI for free


Go to [jules.google.com](jules.google.com) connect Jules to your GitHub account. Create a new repo or fork from another one. Let Jules create a file and folder structure for an Android app with Java Code. You can review the generated files in the `/app/` folder in the repo. You can create an Agents.md file in the root directory for programming rules that will read anytime


> ⚠️ **IMPORTANT:** Always use the planning feature in Jules (rocket icon)! AI instructions surprisingly often implement something different than intended. Good planning significantly improves LM results.

Since simpler AI models (like Gemini 2.5/3 Pro) have weaknesses with complex tasks

If have already code in the repo, because it is a fork, give the task to Jules. Jules analyzes the code and tells you the relevant files.
Copy these files to [lmarena.ai](lmarena.ai). Select "Direct" and then "Claude Opus 4.5 Thinking". Copy the task from Jules and paste it there. Paste Claude's output unchanged back into Jules. Even Gemini 2.5 Pro automatically recognizes where the code belongs and replaced the old one.


## Building the App





You can build only in your fork or repo, otherwise you can't run the workflow. 1. Click on the ⚙️ gear icon (on mobile)
2. Click on **Actions**
3. Select **Android Build** (or the corresponding workflow)
4. Start the build for your branch
> ⏱️ **Duration:** approximately 5 minutes


In case of compilation errors can Gemini 2.5 Pro often fix the errors themselves, if there are no more than 5 errors. If there are much more you need Jules → Claude → Jules

## Tips for Beginners

- ✅ Always work in your own fork – otherwise the workflows won't work
- ✅ Make small changes – easier to debug
- ✅ Always copy error messages completely – the AI needs the context
- ✅ Be patient – sometimes it takes 2-3 iterations
- ✅ Use the planning feature before every major change

---

## Cost Information

| Service | Cost |
|---------|------|
| Gemini 2.5 Pro | Free with a very high limit |
| Gemini 3 Pro | 1 month free trial (cancel in time!) |
