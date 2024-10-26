Design Dash Assistants

This document provides detailed descriptions of each specialized assistant in the Design Dash prototype. It outlines their roles, responsibilities, prompts, settings, and how they interact within the system.

Table of Contents

	•	Coordinator Assistant
	•	Proposal Assistant
	•	Sourcing Assistant
	•	Task and Meeting Assistant
	•	Budget and Finance Assistant
	•	Visualization Assistant
	•	General Prompts and Settings
	•	Glossary

Coordinator Assistant

Description

The Coordinator Assistant acts as the central hub that manages communication between all other assistants. It ensures seamless data flow and task delegation, simplifying the user experience by serving as the primary point of interaction.

Roles and Responsibilities

	•	Communication Management: Oversees the exchange of data between assistants.
	•	Task Delegation: Assigns tasks to the appropriate assistant based on user input or system events.
	•	Context Sharing: Maintains a centralized context with shared client preferences, project specifications, and budgetary guidelines.
	•	Event Handling: Listens for events or changes in the system and triggers appropriate actions in other assistants.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Coordinator Assistant. Your role is to manage communication between specialized assistants in the Design Dash application. You delegate tasks, share context, and ensure data consistency."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.7 (for balanced creativity and coherence)
	•	Max Tokens: 1000
	•	Function Calling: Enabled for interaction with other assistants.
	•	Example Interaction:
	•	User Input: “Update the client’s proposal with the latest budget adjustments.”
	•	Coordinator Action:
	•	Delegates the task to the Proposal Assistant.
	•	Shares updated budget information from the Budget and Finance Assistant.
	•	Notifies the Task and Meeting Assistant to update tasks accordingly.

Proposal Assistant

Description

The Proposal Assistant is responsible for generating and customizing client proposals. It integrates with Bonsai to create proposals tailored to client preferences and project data.

Roles and Responsibilities

	•	Proposal Generation: Creates initial proposal drafts based on project specifications.
	•	Customization: Adjusts proposals according to client preferences and feedback.
	•	Integration: Works with Bonsai for proposal management and incorporates data from other assistants.
	•	Updates and Notifications: Keeps proposals up-to-date with changes from the Budget, Sourcing, and Task Assistants.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Proposal Assistant. Your role is to generate and customize client proposals, integrating with Bonsai and collaborating with other assistants to ensure proposals are accurate and up-to-date."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.6 (to maintain professionalism and accuracy)
	•	Max Tokens: 1500
	•	Function Calling: Enabled for fetching client data and updates.
	•	Example Prompts:
	•	Generating a Proposal:

Generate a proposal for [Client Name] based on the following project details: [Project Details]. Include budget estimates, timelines, and key deliverables.


	•	Updating a Proposal:

Update the proposal for [Client Name] to reflect the approved items and budget adjustments provided by the Budget and Finance Assistant.


	•	Integration with Bonsai:
	•	Uses Bonsai’s API to create, update, and manage proposals.
	•	Fetches client preferences and previous proposals as needed.

Sourcing Assistant

Description

The Sourcing Assistant aids in finding products and materials that match design requirements. It searches for items based on images and criteria such as style, budget, and availability.

Roles and Responsibilities

	•	Product Search: Identifies products similar to provided images or specifications.
	•	Criteria Matching: Filters results based on style, budget, availability, and other client preferences.
	•	Integration with Suppliers: Accesses databases or APIs of suppliers to get real-time information.
	•	Collaboration: Works with the Visualization Assistant to generate visuals of custom design elements.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Sourcing Assistant. Your role is to find products and materials matching design requirements, based on images and criteria like style, budget, and availability."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.7
	•	Max Tokens: 1000
	•	Function Calling: Enabled for image recognition and supplier API integration.
	•	Example Prompts:
	•	Product Search:

Find products similar to the attached image with the following criteria: Style - Modern, Budget - Under $500, Availability - In Stock.


	•	Alternative Suggestions:

Provide alternative product options that meet the same criteria but are under $400 due to budget constraints.


	•	Integration with Image Recognition:
	•	Uses Google Vision API to analyze images and extract features for matching.
	•	Integration with Suppliers:
	•	Accesses supplier APIs to retrieve product details, pricing, and availability.

Task and Meeting Assistant

Description

The Task and Meeting Assistant streamlines project management by recording meeting minutes, summarizing key points, and creating tasks in Asana.

Roles and Responsibilities

	•	Meeting Documentation: Records and summarizes meeting notes.
	•	Task Creation: Generates tasks in Asana based on action items identified in meetings.
	•	Updates and Adjustments: Receives updates from other assistants to modify tasks as needed.
	•	Notifications: Alerts team members about new tasks or changes.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Task and Meeting Assistant. Your role is to document meetings, summarize key points, and create or update tasks in Asana based on the discussions."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.5 (to maintain clarity and conciseness)
	•	Max Tokens: 1000
	•	Function Calling: Enabled for Asana API interactions.
	•	Example Prompts:
	•	Summarizing Meetings:

Summarize the following meeting notes and identify key action items: [Meeting Notes].


	•	Creating Tasks:

Create tasks in Asana for the following action items: [List of Action Items], assigning them to [Assignees] with due dates.


	•	Integration with Asana:
	•	Uses Asana API to create, update, and manage tasks.
	•	Assigns tasks to team members and sets due dates.

Budget and Finance Assistant

Description

The Budget and Finance Assistant manages project budgets, tracks expenses, and coordinates with other assistants to ensure financial accuracy.

Roles and Responsibilities

	•	Budget Tracking: Monitors project budgets and expenditures.
	•	Alerts and Adjustments: Issues alerts for budget overruns and suggests adjustments.
	•	Coordination: Works with the Sourcing Assistant to find cost-effective alternatives.
	•	Reporting: Provides financial summaries and updates to the Proposal Assistant.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Budget and Finance Assistant. Your role is to manage project budgets, track expenses, and coordinate with other assistants to maintain financial accuracy."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.6
	•	Max Tokens: 1000
	•	Function Calling: Enabled for Xero API integration.
	•	Example Prompts:
	•	Budget Update:

Update the budget for [Project Name] with the following expenses: [List of Expenses]. Alert if the total exceeds the allocated budget.


	•	Alternative Suggestions:

Recommend alternative products or solutions to reduce costs by [Amount] while maintaining design integrity.


	•	Integration with Xero:
	•	Uses Xero API to access financial data, update budgets, and track expenses.

Visualization Assistant

Description

The Visualization Assistant enhances design presentations by generating custom images and visualizations using Midjourney’s AI capabilities.

Roles and Responsibilities

	•	Image Generation: Creates custom images based on client preferences, uploaded photos, or mood board elements.
	•	Design Updates: Modifies visualizations as per changes from other assistants or client feedback.
	•	Collaboration: Works with the Sourcing and Proposal Assistants to incorporate visuals into proposals and presentations.

Prompts and Settings

	•	Initialization Prompt:

{
  "role": "system",
  "content": "You are the Visualization Assistant. Your role is to generate custom images and visualizations using Midjourney's AI, enhancing design presentations and proposals."
}


	•	Settings:
	•	Language Model: GPT-4
	•	Temperature: 0.8 (to encourage creativity)
	•	Max Tokens: 1000
	•	Function Calling: Enabled for Midjourney API integration.
	•	Example Prompts:
	•	Generating Visuals:

Create a visualization of a modern living room incorporating the following elements: [List of Elements]. Reflect the client's preference for minimalist design.


	•	Updating Images:

Update the previous visualization to include a different color scheme based on the client's feedback.


	•	Integration with Midjourney:
	•	Uses Midjourney API to generate AI-driven images.
	•	Adjusts parameters based on input criteria and preferences.

General Prompts and Settings

Assistant Interaction

	•	Assistants communicate via the Coordinator Assistant, which manages data flow and task delegation.
	•	All assistants should handle errors gracefully and provide meaningful feedback.

Common Settings

	•	Language Model: GPT-4 for all assistants to ensure consistency.
	•	Temperature: Adjusted per assistant role (see individual settings).
	•	Max Tokens: Set to prevent excessive response lengths.

Function Calling

	•	Enabled: Allows assistants to perform actions such as API calls, data retrieval, and updates.
	•	Usage: Assistants use function calls to interact with external services (e.g., Asana, Xero, Midjourney).

Security and Privacy

	•	Data Handling: Assistants must ensure client data is handled securely and in compliance with relevant regulations.
	•	Authentication: Use secure methods for API authentication, storing keys in environment variables and not in code.

Glossary

	•	Assistant: An AI module specializing in specific tasks within the Design Dash application.
	•	Coordinator Assistant: Central assistant managing communication and task delegation.
	•	Prompt: Instruction or input given to an assistant to perform a task.
	•	Settings: Configuration parameters that determine an assistant’s behavior.
	•	Function Calling: Feature allowing assistants to perform actions like API calls.
	•	API Integration: Connecting with external services through their Application Programming Interfaces.
	•	Temperature: Parameter controlling the randomness of AI responses (lower is more deterministic, higher is more creative).
	•	Max Tokens: Maximum length of the AI’s response.

Conclusion

This document provides detailed information about each assistant in the Design Dash prototype, including their roles, prompts, settings, and integrations. By adhering to these guidelines, you can develop each assistant module effectively and ensure they work cohesively within the application.

