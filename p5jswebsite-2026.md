## The Issue
- [Kendall] - What #432 asks for, in plain English
- [Jaden] - Why it matters to the project: who does it serve and why is it an accessibility question?
- [Des] - Key files in the codebase, and what each does… for ex: src/scripts/builders/reference.ts, astro.config.mjs, src/globals/p5-version.ts, release-workflow-v2.yml
- [Xavier] - Supporting artifacts, if relevant: error messages, console output, screenshots
 
## Documentation Pipeline Overview
- [NIJEL C] - Astro, GitHub Actions/Workflows, any other pieces, and each one’s role
- [Amari] - A system diagram: Docstrings → data.json → website build → dist/ → offline artifact, spanning both repos. Mark the three investigation tracks on it and number them so they are easy to refer back to  
Let's say we wanted to change the documentation of the function `box()`. The end to end process of making a change in the offline reference page goes as follows: find the .js file in the p5.js repository that contains the data you want to change, in our case, the filepath `src/webgl/3d_primitives.js`. After you make your change, if you have npm installed, run `npm run docs` to update the `data.json` file that will be read by the p5.js-website repository. Commit the changes before you move over to the website repository, and with the repositories in the same location, run `npm run custom:dev ../p5.js#main` to connect the two. To generate the local reference, use `npm run build` and open the local host link it gives you when it's finished. This should pull up an offline version of the reference page, and from there, you just navigate to `box()` to check if your change went through.

## Investigation Tracks (three subsections / one per team)
### _Where_ in the build process do we build the offline reference? (Team: JAA)
JAA's scope of technical investigation is in the different workflows, actions, and artifacts that are used to generate different aspects of the project. We mainly used the *New p5.js 2.x release* workflow using the *release-workflow-v2.yml* file that creates the version release notes, along with different tutorials about YAML files, as a reference and guide for our tests.
- [Name] - List all self-directed areas of investigation per team: this section is the point! It's the record of our extensive research and testing
- [Jaden] - Current status of each investigation (do you think it’s a dead end? or is it a promising direction to explore future?)
- [Name] - Code snippets with plain-English explanation, where relevant
### _How_ do we build the offline reference? (Team: TeamFive)
- [NIJEL C] - Restate each team’s scope of technical investigation, referring back to the previous diagram
- [Xavier] - List all self-directed areas of investigation per team: this section is the point! It's the record of our extensive research and testing
- [NIJEL C] - Current status of each investigation (do you think it’s a dead end? or is it a promising direction to explore future?)
- [Des] - Code snippets with plain-English explanation, where relevant
### _What files_ should be in the offline reference? (Team: RawRattlers)
- [Kam] - Restate each team’s scope of technical investigation, referring back to the previous diagram
- [Kendall] - List all self-directed areas of investigation per team: this section is the point! It's the record of our extensive research and testing
- [Mariah] - Current status of each investigation (do you think it’s a dead end? or is it a promising direction to explore future?)
- [Kendall] - Code snippets with plain-English explanation, where relevant
 
## Findings and recommendations
- [NIJEL C] - Summary of options considered, with tradeoffs
- [Mariah] - Anything that we directly verified/tested, like experimental scripts, the size of the generated reference files at present
- [Kam will need help with this] - What we recommend next and why
  - Good place to mention what would be a reasonable size for the .zip
  - Also a good place to share thoughts on including all images, search functionality, language support, etc.
- [Name] - Suggested three sub-issues for Kit to add, informed by our research
