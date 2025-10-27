# My Git Mastery Challenge Journey

## Student Information
- Name: Krishna Tulasi Satti
- Student ID: 23A91A05C5
- Repository: https://github.com/KrishnaTulasiSatti/git-solved-23A91A05C5
- Date Started: 25-10-2025
- Date Completed: 27-10-2025

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all 
merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|----------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 2 | Copy specific commit |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used port 8080, development used 3000
- **Resolution**: Created unified config with environment-based settings
- **Strategy**: Keep production as default, add dev as optional
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Different database hosts and SSL modes
- **Resolution**: Created separate profiles for production and development
- **Strategy**: Restructured JSON to support both environments
- **Difficulty**: Medium
- **Time**: 10 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Different deployment strategies (production vs docker-compose)
- **Resolution**: Added conditional logic based on DEPLOY_ENV variable
- **Strategy**: Made script handle both environments dynamically
- **Difficulty**: Hard
- **Time**: 20 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Different monitoring intervals and log formats
- **Resolution**: Environment-based configuration object
- **Strategy**: Used process.env.NODE_ENV to determine behavior
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 5: docs/architecture.md
- **Issue**: Different architectural descriptions
- **Resolution**: Merged both descriptions into comprehensive document
- **Strategy**: Created sections for each environment
- **Difficulty**: Easy
- **Time**: 10 minutes

#### Conflict 6: README.md
- **Issue**: Different feature lists and version numbers
- **Resolution**: Combined all features with clear environment labels
- **Strategy**: Organized features by category
- **Difficulty**: Easy
- **Time**: 10 minutes

### Merge 2: main + conflict-simulator (6 files)

#### Conflict 1: `config/app-config.yaml`
- **Issue**: Simulator branch introduced dynamic port allocation conflicting with static port in main  
- **Resolution**: Unified config with conditional port assignment based on environment  
- **Strategy**: Default to static port `8080`, override with dynamic if `SIMULATOR_MODE` is enabled  
- **Difficulty**: Medium  
- **Time**: 14 minutes  

#### Conflict 2: `config/database-config.json`
- **Issue**: Simulator used mock DB host and disabled SSL, conflicting with production settings  
- **Resolution**: Added `SIMULATOR_DB` profile with mock settings alongside production profile  
- **Strategy**: Structured JSON to support multiple profiles with clear environment toggles  
- **Difficulty**: Medium  
- **Time**: 12 minutes  

#### Conflict 3: `scripts/deploy.sh`
- **Issue**: Simulator used local Docker deployment, main used cloud CLI  
- **Resolution**: Added deployment mode switch using `DEPLOY_ENV=simulator|production`  
- **Strategy**: Modularized script with separate functions for each deployment strategy  
- **Difficulty**: Hard  
- **Time**: 22 minutes  

#### Conflict 4: `scripts/monitor.js`
- **Issue**: Simulator used verbose logging and short intervals, main used minimal logs  
- **Resolution**: Created config object to toggle logging level and interval based on mode  
- **Strategy**: Used `process.env.SIMULATOR_MODE` to control behavior  
- **Difficulty**: Medium  
- **Time**: 16 minutes  

#### Conflict 5: `docs/architecture.md`
- **Issue**: Simulator added new flow diagrams and async event handling, main had legacy sync model  
- **Resolution**: Merged both into a comparative architecture section  
- **Strategy**: Created side-by-side diagrams and explained evolution from sync to async  
- **Difficulty**: Easy  
- **Time**: 11 minutes  

#### Conflict 6: `README.md`
- **Issue**: Simulator added new feature descriptions and versioning, main had outdated info  
- **Resolution**: Combined all features with version labels and simulator highlights  
- **Strategy**: Organized features by category and added simulator-specific notes  
- **Difficulty**: Easy  
- **Time**: 10 minutes  

## Most Challenging Parts

1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. **Testing After Resolution**: Making sure resolved code actually worked was crucial.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- When in doubt, ask for clarification
- Document your resolution strategy
- Keep calm and read carefully

## Reflection
This challenge taught me that merge conflicts aren't scary - they're 
just Git asking "which version do you want?". The key is understanding 
what each side is trying to do before combining them. I now feel 
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and 
cherry-pick) was invaluable. I understand the difference between merge 
and rebase, and when to use each. Most importantly, I learned that 
git reflog is a lifesaver!
