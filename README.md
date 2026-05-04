# AI-sort-labdata
A "skill" markdown can be copy-paste to a AI agent to sort your lab data into both human readable markdown table and a machine readable JSON file

---
## How to use this skill:
1. **Copy the code block in the [Skill.md](Skill.md) above.**
2. **Paste it into a new "Custom Instruction" or "Agent System Prompt"** in your AI tool of choice.
3. **To trigger it**, simply paste your list of filenames and their creation dates. For example: 
   > "Hey, parse these for my Notion: 
   > 1. RMN_WS2-S1_532 100x 1s_spot1.wdf (Created: June 30, 10:00 AM)
   > 2. SEM_WS2-S1_5kV Inlens 10000x_lowmag.tif (Created: June 30, 09:00 AM)"

The AI will now automatically detect that the SEM was done *before* the Raman and give you the table, the JSON, and the artifact warning you requested!
