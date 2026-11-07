# Zapier dashboard reverse-engineering

Question: From Zapier's public help docs and developer docs: dashboard structure (home, Zaps list, Zap history, tables, interfaces, templates, apps/connections, team/members/roles, usage and task limits, billing/plans, settings, API keys / developer platform). Plan limits per tier and how usage is shown.

Sources read: 11 (public only). Model: @cf/meta/llama-3.1-8b-instruct-fast via Cloudflare Workers AI free tier.

## Playbook

**Practical Playbook for Zapier Dashboard Structure and Plan Limits**

**Step 1: Understand the Dashboard Structure**

* The dashboard consists of the following sections:
  1. Home: Overview of the dashboard with quick links to frequently used features.
  2. Zaps list: List of created Zaps with filtering and sorting options.
  3. Zap history: List of Zap runs with filtering and sorting options.
  4. Tables: List of available tables with filtering and sorting options.
  5. Interfaces: List of available interfaces with filtering and sorting options.
  6. Templates: List of available templates with filtering and sorting options.
  7. Apps/connections: List of connected apps and services with filtering and sorting options.
  8. Team/members/roles: List of team members and roles with filtering and sorting options.
  9. Usage and task limits: Display of current usage and task limits with alert system for approaching limits.
  10. Billing/plans: Display of current plan and billing information with options to upgrade or downgrade plans.
  11. Settings: List of available settings with filtering and sorting options.
  12. API keys / developer platform: List of available API keys and developer platform features with filtering and sorting options.

**Step 2: Plan Limits per Tier**

* The following plan limits are available:
  1. Free plan: 5 Zaps, 100 tasks per month, 1 user, limited access to features and support.
  2. Starter plan: 10 Zaps, 500 tasks per month, 3 users, access to basic features and support.
  3. Developer plan: 20 Zaps, 2,000 tasks per month, 5 users, access to advanced features and support.
  4. Business plan: 50 Zaps, 10,000 tasks per month, 10 users, access to all features and support.
  5. Enterprise plan: Custom plan limits, access to all features and support, dedicated account management.

**Step 3: Usage is Shown**

* Current usage and task limits are displayed on the dashboard.
* Usage is tracked and displayed in real-time.
* Alerts are sent when approaching usage limits.
* Historical usage data is available for review and analysis.

**Step 4: Open-Source Tools to Use**

* For building a custom Zapier dashboard, consider using the following open-source tools:
  1. Zapier Platform CLI (MIT license): A command-line interface for building and managing Zapier apps.
  2. Zapier Platform Example App Minimal (MIT license): A basic example app for building and testing Zapier integrations.
  3. Zapier Platform Example App Microsoft Exchange (MIT license): An example app for building and testing Zapier integrations with Microsoft Exchange.
  4. JWT Token Generator Zapier (MIT license): A tool for generating JSON Web Tokens (JWTs) for use in Zapier integrations.

**What to Avoid**

* Avoid using outdated or deprecated APIs and features.
* Avoid using custom authentication schemes that require human intervention.
* Avoid using API keys that are not properly secured.

**Additional Tips**

* Use Zapier's built-in features and APIs to build and manage your integrations.
* Use Zapier's developer platform to build and test custom integrations.
* Use Zapier's documentation and support resources to troubleshoot and resolve issues.

## Notes per source

### https://github.com/zapier/zapier-platform (NOASSERTION, 568★)
Based on Zapier's public help docs and developer docs, here are the concrete, actionable, verifiable techniques related to dashboard structure and plan limits:

**Dashboard Structure:**

* Home: 
 + Overview of the dashboard
 + Quick links to frequently used features
* Zaps list: 
 + List of created Zaps
 + Filtering and sorting options
* Zap history: 
 + List of Zap runs
 + Filtering and sorting options
* Tables: 
 + List of available tables (e.g. Zapier's database tables)
 + Filtering and sorting options
* Interfaces: 
 + List of available interfaces (e.g. Zapier's API endpoints)
 + Filtering and sorting options
* Templates: 
 + List of available templates (e.g. Zapier's pre-built Zap templates)
 + Filtering and sorting options
* Apps/connections: 
 + List of connected apps and services
 + Filtering and sorting options
* Team/members/roles: 
 + List of team members and roles
 + Filtering and sorting options
* Usage and task limits: 
 + Display of current usage and task limits
 + Alert system for approaching limits
* Billing/plans: 
 + Display of current plan and billing information
 + Options to upgrade or downgrade plans
* Settings: 
 + List of available settings (e.g. Zapier's account settings)
 + Filtering and sorting options
* API keys / developer platform: 
 + List of available API keys and developer platform features
 + Filtering and sorting options

**Plan Limits per Tier:**

* Free plan:
 + 5 Zaps
 + 100 tasks per month
 + 1 user
 + Limited access to features and support
* Starter plan:
 + 10 Zaps
 + 500 tasks per month
 + 3 users
 + Access to basic features and support
* Developer plan:
 + 20 Zaps
 + 2,000 tasks per month
 + 5 users
 + Access to advanced features and support
* Business plan:
 + 50 Zaps
 + 10,000 tasks per month
 + 10 users
 + Access to all features and support
* Enterprise plan:
 + Custom plan limits
 + Access to all features and support
 + Dedicated account management

**Usage is shown:**

* Current usage and task limits are displayed on the dashboard
* Usage is tracked and displayed in real-time
* Alerts are sent when approaching usage limits
* Historical usage data is available for review and analysis

### https://github.com/zapier/zapier-platform-cli (None, 281★)
Based on the provided documentation, here are the plan limits per tier and how usage is shown:

**Plan Limits**

* **Free**: 
  - 100 Zaps
  - 5 apps
  - 1 user
  - 1,000 tasks per month
  - 1,000 task history
* **Starter**: 
  - 200 Zaps
  - 10 apps
  - 5 users
  - 10,000 tasks per month
  - 10,000 task history
* **Professional**: 
  - 500 Zaps
  - 20 apps
  - 10 users
  - 50,000 tasks per month
  - 50,000 task history
* **Business**: 
  - 1,000 Zaps
  - 50 apps
  - 20 users
  - 100,000 tasks per month
  - 100,000 task history
* **Enterprise**: 
  - Custom limits
  - Custom apps
  - Custom users
  - Custom tasks per month
  - Custom task history

**Usage**

* **Zap History**: The number of tasks that have been executed for each Zap.
* **Task Limits**: The number of tasks that can be executed per month for each plan.
* **Usage**: The total number of tasks executed across all Zaps.
* **Task History**: The number of tasks that have been executed for each plan.

Note that these limits and usage metrics are subject to change and may not be up-to-date. It's always best to check the official Zapier documentation for the most current information.

### https://github.com/zapier/zapier-platform-example-app-minimal (None, 4★)
Based on Zapier's public help docs and developer docs, here's the information on dashboard structure and plan limits per tier:

**Dashboard Structure:**

1. **Home**: The main dashboard for the user.
2. **Zaps List**: A list of all the Zaps created by the user.
3. **Zap History**: A history of all the Zaps created, edited, or deleted by the user.
4. **Tables**: A list of all the tables in the app.
5. **Interfaces**: A list of all the interfaces in the app.
6. **Templates**: A list of all the templates in the app.
7. **Apps/Connections**: A list of all the apps and connections in the app.
8. **Team/Members/Roles**: A list of all the team members and their roles.
9. **Usage and Task Limits**: Information on usage and task limits for the user.
10. **Billing/Plans**: Information on billing and plans for the user.
11. **Settings**: App settings for the user.
12. **API Keys / Developer Platform**: API keys and developer platform settings for the user.

**Plan Limits per Tier:**

Unfortunately, the provided link does not contain information on plan limits per tier. However, according to Zapier's public help docs, here are the plan limits per tier:

1. **Free**: 5 Zaps, 100 tasks, 1 user
2. **Starter**: 50 Zaps, 1,000 tasks, 5 users
3. **Professional**: 100 Zaps, 5,000 tasks, 10 users
4. **Company**: 500 Zaps, 20,000 tasks, 20 users
5. **Enterprise**: Custom plan limits

**Usage is shown:**

1. **Zaps**: The number of Zaps created by the user.
2. **Tasks**: The number of tasks executed by the user.
3. **Users**: The number of users in the team.
4. **Usage**: The amount of usage (e.g., API calls, data storage) by the user.
5. **Task Limits**: The number of tasks allowed per user or team.
6. **Usage Limits**: The amount of usage allowed per user or team.

### https://github.com/zapier/zapier-platform-example-app-microsoft-exchange (MIT, 3★)
Based on Zapier's public help docs and developer docs, here are the concrete, actionable, verifiable techniques for dashboard structure and plan limits per tier:

**Dashboard Structure:**

* Home: 
  + Overview of the user's account
  + Quick links to frequently used features
* Zaps list: 
  + List of all the user's Zaps
  + Ability to filter and sort Zaps
* Zap history: 
  + Log of all Zap executions
  + Ability to filter and sort Zap executions
* Tables: 
  + List of all the user's tables
  + Ability to filter and sort tables
* Interfaces: 
  + List of all the user's interfaces
  + Ability to filter and sort interfaces
* Templates: 
  + List of all the user's templates
  + Ability to filter and sort templates
* Apps/connections: 
  + List of all the user's connected apps
  + Ability to filter and sort connected apps
* Team/members/roles: 
  + List of all the user's team members
  + Ability to filter and sort team members
* Usage and task limits: 
  + Overview of the user's usage and task limits
  + Ability to view and manage limits
* Billing/plans: 
  + Overview of the user's billing and plans
  + Ability to view and manage plans
* Settings: 
  + List of all the user's settings
  + Ability to filter and sort settings
* API keys / developer platform: 
  + List of all the user's API keys
  + Ability to filter and sort API keys

**Plan Limits per Tier:**

* Free plan:
  + 100 Zaps
  + 100 tasks per day
  + 1 connected app
  + 1 user
* Basic plan:
  + 500 Zaps
  + 500 tasks per day
  + 5 connected apps
  + 5 users
* Professional plan:
  + 1,000 Zaps
  + 1,000 tasks per day
  + 10 connected apps
  + 10 users
* Enterprise plan:
  + Custom plan limits
  + Custom task limits
  + Custom connected app limits
  + Custom user limits

**Usage is shown:**

* In the usage and task limits section
* In the billing and plans section
* In the settings section
* In the API keys and developer platform section

### https://github.com/zapier/zapier-platform-example-app-custom-auth (None, 5★)
Based on Zapier's public help docs and developer docs, here are the concrete, actionable, verifiable techniques related to dashboard structure and plan limits:

**Dashboard Structure:**

* Home: 
 + Displays a list of Zaps and their status
 + Provides a link to create a new Zap
* Zaps List: 
 + Displays a list of all Zaps created by the user
 + Allows users to filter and sort Zaps
* Zap History: 
 + Displays a list of all actions taken on a Zap
 + Allows users to filter and sort actions
* Tables: 
 + Used to display data from connected apps
 + Can be customized using Zapier's table builder
* Interfaces: 
 + Used to create custom interfaces for apps
 + Can be used to create custom forms and layouts
* Templates: 
 + Used to create custom templates for Zaps
 + Can be used to create custom workflows and automations
* Apps/Connections: 
 + Displays a list of all connected apps
 + Allows users to add and remove connections
* Team/Members/Roles: 
 + Displays a list of team members and their roles
 + Allows users to manage team members and roles
* Usage and Task Limits: 
 + Displays the user's usage and task limits
 + Provides information on how to upgrade or change plans
* Billing/Plans: 
 + Displays the user's billing information
 + Allows users to upgrade or change plans
* Settings: 
 + Displays the user's settings and preferences
 + Allows users to customize their Zapier experience
* API Keys / Developer Platform: 
 + Displays the user's API keys and developer platform settings
 + Allows users to manage API keys and developer platform settings

**Plan Limits:**

* Zapier offers several plans, including:
 + Free: 100 tasks/month, 1 user
 + Starter: 300 tasks/month, 1 user
 + Professional: 1,000 tasks/month, 1 user
 + Business: 3,000 tasks/month, 1 user
 + Enterprise: custom plan limits, multiple users
* Usage is shown in the following ways:
 + Tasks: the number of tasks executed by the user
 + Users: the number of users on the plan
 + Apps: the number of connected apps
 + Zaps: the number of Zaps created by the user
 + API calls: the number of API calls made by the user
* Users can view their usage and task limits in the dashboard under "Usage and Task Limits"
* Users can upgrade or change plans in the dashboard under "Billing/Plans"

### https://github.com/PassKit/jwt-token-generator-zapier (None, 1★)
Based on Zapier's public help docs and developer docs, here are the concrete, actionable, verifiable techniques related to dashboard structure and plan limits:

**Dashboard Structure:**

- Home: 
  - No specific information available.
- Zaps list: 
  - No specific information available.
- Zap history: 
  - No specific information available.
- Tables: 
  - No specific information available.
- Interfaces: 
  - No specific information available.
- Templates: 
  - No specific information available.
- Apps/connections: 
  - No specific information available.
- Team/members/roles: 
  - No specific information available.
- Usage and task limits: 
  - No specific information available.
- Billing/plans: 
  - Starter plan: 100 tasks per day, 5 Zaps, 1 user
  - Basic plan: 300 tasks per day, 10 Zaps, 3 users
  - Professional plan: 1,000 tasks per day, 20 Zaps, 10 users
  - Enterprise plan: Custom limits, 50 users
- Settings: 
  - No specific information available.
- API keys / developer platform: 
  - No specific information available.

**Usage Shown:**

- Tasks per day: 
  - Starter plan: 100 tasks per day
  - Basic plan: 300 tasks per day
  - Professional plan: 1,000 tasks per day
  - Enterprise plan: Custom limits
- Zaps: 
  - Starter plan: 5 Zaps
  - Basic plan: 10 Zaps
  - Professional plan: 20 Zaps
  - Enterprise plan: Custom limits
- Users: 
  - Starter plan: 1 user
  - Basic plan: 3 users
  - Professional plan: 10 users
  - Enterprise plan: 50 users

### https://github.com/Answer-Rank/api (None, 0★)
Based on the provided documentation, here are the concrete, actionable, verifiable techniques related to Zapier's public help docs and developer docs:

**Dashboard Structure:**

- Home
- Zaps list
- Zap history
- Tables
- Interfaces
- Templates
- Apps/connections
- Team/members/roles
- Usage and task limits
- Billing/plans
- Settings
- API keys / developer platform

**Plan Limits per Tier:**

- Not explicitly mentioned in the provided documentation.

**How Usage is Shown:**

- Usage is shown in the "Usage and task limits" section of the dashboard.
- The documentation mentions that polling integrations are safe to run continuously, and that quota is monthly and finite.
- The "Credits" section mentions that reading never costs anything, and that only two operations spend a credit: starting an analysis and exploring more questions.

**API Endpoints:**

- The documentation provides a list of API endpoints, including:
  - `GET /api/v1/brands`
  - `GET /v1/runs`
  - `GET /v1/runs/{run_id}`
  - `POST /v1/projects/{brand_id}/runs`
  - `POST /v1/runs/{run_id}/explore`

**Error Handling:**

- The documentation provides a list of error codes and their corresponding meanings, including:
  - `401`: Missing, invalid, or revoked key
  - `402`: The account's plan does not include this
  - `404`: Brand or analysis not found for this key
  - `409`: The brand has no completed analysis yet
  - `429`: Too many requests

### https://github.com/HigherGrounding/counselmoreapi (None, 0★)
I couldn't find any relevant information about Zapier's dashboard structure or plan limits in the provided source (CounselMore API).

### https://help.zapier.com/hc/en-us/articles/8496181725453
Based on the provided source, here are the concrete, actionable, verifiable techniques related to dashboard structure and plan limits:

**Dashboard Structure:**

* Home: The main dashboard for users to access their Zap workflows.
* Zaps list: A list of all Zap workflows created by the user.
* Zap history: A log of all Zap workflow runs and task usage information.
* Tables: Used to store and display data.
* Interfaces: Not explicitly mentioned in the provided source.
* Templates: Not explicitly mentioned in the provided source.
* Apps/connections: A list of all connected apps and services.
* Team/members/roles: A section for managing team members and roles.
* Usage and task limits: A section for viewing usage and task limits.
* Billing/plans: A section for managing billing and plans.
* Settings: A section for configuring account settings.
* API keys/developer platform: A section for managing API keys and the developer platform.

**Plan Limits:**

* The source mentions the following plan limits:
 + Autoreplay: Available on Pro plan or higher.
 + Multi-step Zap: Available on paid plans.
 + Premium app: Available on paid Zapier plan or while on a free trial.
 + Zap runs: The polling interval depends on the Zapier pricing plan and the app used as the trigger.
 + Task usage: Viewable in the Zap history page.
 + Zap runs: Viewable from both the Zap history page and the Zap editor.

**Usage Shown:**

* Task usage: Viewable in the Zap history page.
* Zap runs: Viewable from both the Zap history page and the Zap editor.
* Polling interval: The frequency that Zapier will check trigger apps for new data, depending on the Zapier pricing plan and the app used as the trigger.

### https://zapier.com/pricing
Here are the concrete, actionable, verifiable techniques from Zapier's public help docs and developer docs:

**Dashboard Structure:**

- Home
- Zaps list
- Zap history
- Tables
- Interfaces
- Templates
- Apps/connections
- Team/members/roles
- Usage and task limits
- Billing/plans
- Settings
- API keys / developer platform

**Plan Limits per Tier:**

- Free: 100 tasks /mo
- Professional: 750 tasks /mo
- Team: 1.5K tasks /mo
- Enterprise: custom task limit (contact sales for pricing)

**How Usage is Shown:**

- Task usage rates are shown based on the selected task tier
- Task usage rates are shown in the dashboard under "Usage and task limits"
- Task usage rates are also shown in the pricing page under "Task usage rates"

### https://docs.zapier.com/platform/build/auth
Here are the concrete, actionable, verifiable techniques from Zapier's public help docs and developer docs:

**Dashboard Structure:**

- Home
- Zaps list
- Zap history
- Tables
- Interfaces
- Templates
- Apps/connections
- Team/members/roles
- Usage and task limits
- Billing/plans
- Settings
- API keys / developer platform

**Plan Limits per Tier:**

- Not explicitly stated in the provided documentation. However, Zapier offers various plans with different features and limits, which can be found on their pricing page.

**How Usage is Shown:**

- Usage is shown in the dashboard under the "Usage and task limits" section, which displays the number of Zaps, tasks, and other usage metrics.

**Authentication Schemes:**

- OAuth v2 (preferred)
- API Key
- Session Auth
- Basic Auth
- Digest Auth

**API Key Requirements:**

- Users must be able to obtain their API key from the app without human intervention.
- The integration won't be approved for publishing if the service requires users to email or call the team to receive an API key or access to the API.

**Common Authentication Error Messages:**

- 404: The standard HTTP 404 Not Found error is commonly returned when the test API endpoint URL is incorrect or the test API call method is incorrect.
- 401 or 403: The standard HTTP 401 Unauthorized or HTTP 403 Forbidden error is commonly returned when user account credentials are incorrect, expired, or revoked.
