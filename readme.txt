Prompt Generator Suite
======================

This package contains three AutoHotkey scripts that automatically generate creative image prompts for use in Stable Diffusion or similar tools. Each script assembles prompts using randomized attributes from .txt files and copies the finished prompt into Notepad++ for easy access and further editing.

-----------------------------------------------------------------------
CONTENTS

1. MasterPromptNSFW_Context.ahk
2. MasterPromptNSFW_Random.ahk
3. MasterPromptSFW.ahk

-----------------------------------------------------------------------
SCRIPT DESCRIPTIONS AND DIFFERENCES

1. MasterPromptNSFW_Context.ahk
   Generates NSFW (adult) prompts with context-aware filtering.
   Facial expressions and lighting are dynamically chosen to fit the sex act and environment, making results more realistic and visually coherent.
   For example: If the scene is a bedroom, lighting will be "indoor" or "cozy". If the sex act is intense, only appropriate facial expressions will be picked (such as "ahegao", "lewd", "moaning").
   Use this script if you want prompts that always make sense.

2. MasterPromptNSFW_Random.ahk
   Generates NSFW prompts with a fully random approach.
   All attributes (including facial expressions and lighting) are picked randomly, with no regard for scene context or logic.
   Much simpler and easier to edit or expand by just adding or removing modules in the scripts array.
   Use this script if you want a simple, modular setup and do not mind occasionally mismatched prompts.

3. MasterPromptSFW.ahk
   Generates SFW (Safe For Work) prompts. Content will avoid explicit tags and focus on wholesome or artistic descriptions.
   Randomizes all features (hair, clothing, setting, etc.) for general creative output.
   Suitable for all audiences and for sharing without NSFW risk.

-----------------------------------------------------------------------
IMPORTANT: SETTING THE CORRECT PATH

You must edit the folder and file paths in every script so they match where you have saved your files. The default path in these scripts is:

    D:\AI\Billeder Til Scripts\RandomPrompt\Scripts\

This is just an example from the original creator’s computer. If you move or store your scripts and .txt files anywhere else, you must update the path in every script.

How to Edit the Path:

1. Decide where you want to keep your scripts and .txt files, for example: C:\Users\YourName\PromptGenerator\
2. Open each main prompt generator .ahk script (MasterPromptNSFW_Context.ahk, MasterPromptNSFW_Random.ahk, MasterPromptSFW.ahk) in Notepad++ or your preferred text editor.
3. Press Ctrl+F (Find) on Windows, Cmd+F on Mac, or Ctrl+F on Linux.
4. Search for this text:
       D:\AI\Billeder Til Scripts\RandomPrompt\Scripts\
5. Replace every instance with the folder path where you have saved your scripts.

Example:
If you keep everything in C:\Users\Bob\PromptSuite\Scripts\, you must change all paths to:
    C:\Users\Bob\PromptSuite\Scripts\

6. Save the file when done.

-----------------------------------------------------------------------
IMPORTANT: SUB-SCRIPTS AND .TXT FILE PATHS

Each tag sub-script (for example, facialexpression.ahk, hairstyles.ahk, etc.) reads from a specific .txt file.
By default, these are set to something like:

    D:\AI\Billeder Til Scripts\RandomPrompt\facialexpression.txt
    D:\AI\Billeder Til Scripts\RandomPrompt\hairstyles.txt
    and so on.

You must update the path in EVERY sub-script so it points to the actual location of your .txt files.
Open each sub-script in your text editor.
Search for D:\AI\Billeder Til Scripts\RandomPrompt\ and replace it with your own folder path.
Repeat for every sub-script and every .txt file used.

Be thorough: If you move the .txt files or change folder names, you must update every path reference in every sub-script.

-----------------------------------------------------------------------
HOW TO USE

1. Requirements
   See requirements.txt for full details.

2. Setup
   Place all main scripts, sub-scripts, and .txt files in your chosen directories. Make sure all paths in the scripts point to the right folders.

3. Running a Script
   Double-click your chosen .ahk script to run it.
   The script will open Notepad++ (or a new tab if already open).
   Prompts will be generated and pasted into Notepad++, one per line (or tab), depending on the script and your prompt count.

4. Setting the Number of Prompts
   Open the script you want to use with a text editor.
   Look for the line near the top that says:
       promptCount := 5  ; Change this to any number you want!
   Change the number (for example, 10 for ten prompts), save the script, and rerun it.

5. Editing or Expanding the Scripts
   To add or remove categories (like hairstyles or jewelry), edit the list of included scripts in the relevant .ahk file:
     In MasterPromptNSFW_Random.ahk, look for the scripts := [] array and add or remove filenames as needed.
     In the other scripts, tags are hardcoded in order—edit the script where each module is called.
   If you change the contents of any .txt file, your changes will automatically take effect the next time you generate prompts.
   If you add a new .txt file, make sure to add a corresponding script call (or update the scripts array if using the modular random script).

6. Important Notes
   The NSFW scripts are intended for adults only.
   If you share with others, make sure to provide all the required .txt data files for the scripts to work.
   If you make large changes, test your script to ensure all prompts are generated as expected.

-----------------------------------------------------------------------
TROUBLESHOOTING

Notepad++ does not open a new tab for each prompt:
    You must be using Windows 11 and Notepad++ (see requirements.txt).
    If Notepad++ is not found, the script may open standard Notepad instead.

Clipboard errors or missing tags:
    Make sure all .txt files are present and formatted correctly (comma-separated, no trailing blank lines).
    If prompts are incomplete, check for typos in the script or .txt filenames.

Prompts are too random or mismatched:
    Use MasterPromptNSFW_Context.ahk for more realistic and sensible results.

-----------------------------------------------------------------------
Enjoy your automatic prompt generation!
