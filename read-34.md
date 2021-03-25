# Back End Deployment

## Django Settings Best Practices

method1 - settings directory seperating sharable from non-sharable settings.
- Pros:
  - All environments are in VCS.
  - Easy to share settings.
- Cons:
  - Have to hide secret passwords and tokens.
  - "Inheritance" of settings can be hard to trace and maintain

method2 - using environment variables solves the issue of hiding secret password and tokens, but comes with manual type conversions and handling of KeyError exceptions
- Pros:
  - Configuration seperate from code.
  - Uses the same code for all environments.
  - No need to deal with inheritance in settings.
  - 'There is a theoretical grounding for using invironment variables -- 12 factors'??? What does this mean???
- Cons:
  - Need to share default 'config' (configurations?) between devs.

12 Factors - A collection of recommendations by Heroku on how to build distributed web-apps that will be easy to deploy and scale in the cloud.
1. Codebase
2. Dependencies
3. Config
4. Backing Services
5. Build, release, run
6. Processes
7. Port Binding
8. Concurrency
9. Disposability
10. Dev/prod Parity
11. Logs
12. Admin Processes

Django-environ - Replaces os.environ to eliminate the need to handle errors caused by os incompatibility. This is technically a merge of the following tools:
- envparse
- honcho
- dj-database-url
- dj-search-url
- dj-config-url
- django-cache-url

Django Settings Best Practices:
- Keep settings in environment variables.
- Set defaults to environment variables.
- Don't hardcode sensitive settings, and don't put them in VCS
- Split Settings into groups (Django, third-party, project, etc.).
- Follow naming conventions for custom settings.

VCS (Version Control System) - Is a system for managing revisions of/changes to code. Is ours GitHub, Git, or some combination of the two?