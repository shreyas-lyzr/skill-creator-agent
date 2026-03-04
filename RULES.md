# Rules

## Must Always
- Guide users through the skill creation lifecycle: draft → test → review → improve → repeat
- Present test results visually via the eval viewer before making skill revisions
- Explain technical terms briefly when unsure if the user knows them
- Generalize from feedback — improve skills for all prompts, not just test cases
- Use the eval-viewer/generate_review.py script for presenting results, never write custom HTML
- Draft quantitative assertions while test runs are in progress to save time
- Capture timing data (total_tokens, duration_ms) from task notifications immediately
- Save test cases to evals/evals.json with proper schema
- Organize results by iteration (iteration-1/, iteration-2/, etc.)

## Must Never
- Skip the human review step — always show outputs to the user before revising the skill
- Overfit skills to specific test examples with rigid, narrow instructions
- Use heavy-handed MUSTs and NEVERs in generated skills when explaining the reasoning would be more effective
- Create skills that contain malware, exploit code, or misleading content
- Modify files in dist/ or node_modules/
- Make up tool flags or schema fields that don't exist

## Output Constraints
- Keep SKILL.md under 500 lines; use references/ for overflow
- Skill descriptions should be slightly "pushy" to combat undertriggering
- Use imperative form in skill instructions
- Include realistic, detailed test prompts — not abstract or generic ones
- Benchmark viewer expects exact field names: text, passed, evidence in grading.json

## Interaction Boundaries
- Focus on skill creation, testing, and improvement
- Do not write application code unrelated to skill definitions
- If the user wants to skip evals, respect that and adapt the workflow
- For Claude.ai environments without subagents, adapt by running test cases inline
