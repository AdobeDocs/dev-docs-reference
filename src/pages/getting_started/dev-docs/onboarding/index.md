# Dev Docs Onboarding

## The Basics for DevDocs
- All content resides in the public https://github.com/orgs/AdobeDocs/ repo.
- A (non-corp) GitHub account is required to author content. (What that means is that the public repositories that power the Developer Website are not behind the firewall or on the .corp github that internal adobe users use.  The repo lives in the non-corp github. There's no cross over between corp and non-corp.You can use whatever email you want with non-corp github, as long as you have a username on github.) 
- Content is authored using Markdown.
  - We are researching additional authoring options for the future
- All authors need to sign the Adobe Contributor License Agreement (CLA)
- Questions & Support: #adobe-developer-website

## How to create a website utilizing DevDocs on the Adobe Developer Website
- **Getting Started**:
  - Before you begin, ensure you have:
    - A GitHub account (different from your git.corp.adobe.com account)
    - Your team's GitHub usernames or emails for content authors/owners
    - Learn About the System and familiarize yourself with the Adobe Developer Website DevDocs reference library 
- **Submit a JIRA ticket**:
  - Submit a [JIRA ticket](https://jira.corp.adobe.com/secure/RapidBoard.jspa?rapidView=31350&projectKey=DEVSITE&view=planning&issueLimit=100) to get started. Include the following on the JIRA ticket: 
    - Team: 
    - Primary Contact(s): 
    - Primary Contact GitHub account(s)(not Corp GitHub): 
    - Contributors:
    - Contributor GitHub accounts:
    - Desired Repository Name(s):
    - Desired Path Prefix:
      - The pathprefix defines the URL for their microsite, e.g.  https://developer-dev.adobe.com/my-path-prefix/. It’s usually the same as repo name (but not always)
      - Some repos where they differ: pathPrefix: “/developer-console/docs”, repo: “adobe-dev-console”,`
- **What happens next:**:
  - Engineering will process your request and set up your team and repositories.
  - If more information is needed, please watch the JIRA ticket for comments. 
  - Next Steps: 
    1. Check your email or GitHub notifications for an invite to join the [AdobeDocs organization](https://github.com/orgs/AdobeDocs/teams) 
                        Important: Explicitly accept the invite to gain access. The invite will only be valid for 7 days. 
    2. Wait for confirmation that you've been added to the organization
- **For New Teams**: 
  - Create a new team with your direct contacts as "Maintainers"
  - Create a sub-team for content authors
  - Set up team permissions so maintainers can add/remove content authors
  - Create and configure repository(ies) for your team
- **Start Writing Content**:
  - Once your repository is set up, you can begin creating content. See DevDocs Reference Library https://developer-stage.adobe.com/dev-docs-reference/  for information on how to get started! 
  - Note: Engineering handles all repository configuration and setup. As a content author, you only need to focus on writing, building and deploying your content. 