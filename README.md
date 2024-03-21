# World Health Org Metrics Project 

## Problem Statement

The World Health Organization leads global efforts to expand universal health coverage. They direct and coordinate the world’s response to health emergencies however there is currently no integrated digital environment for public health experts from all around the globe to collaborate on pandemic and epidemic intelligence and ongoing public health emergency events. The World Health Organization is exploring how to easily collaborate with external experts around the world to work on public health issues like COVID-19.

## Goal

Monitor open source health across different projects to have a high level view the best practices adopted by various open source projects to help build interest in open source work and advocate for more open source development

Issue Project  [here](https://github.com/github/SI-skills-based-volunteering/issues/147#issuecomment-1472370039)

## Team
<table>
  <tr valign="top">
  <td align=center>
    <img src="https://avatars.githubusercontent.com/u/12959012?v=4" width="110" height="110"><br/>
      <a href="https://github.com/liliana3186">@liliana3186</a><br/>
     Liliana Torres<br/>
      <b>Project Lead, Senior Data Analyst </b>
    </td>
    <td align=center>
    <img src="https://avatars.githubusercontent.com/u/34780972?v=4" width="110" height="110"><br/>
      <a href="https://github.com/hasan-dot">@hasan-dot</a><br/>
      Hassan Hawache<br/>
      <b>Sofware Engineer III</b>
    </td>
    <td align=center>
    <img src="https://avatars.githubusercontent.com/u/61184284?v=4" width="110" height="110"><br/>
      <a href="https://github.com/darostegui">@darostegui</a><br/>
      Diego Arostegui<br/>
      <b>Customer Reliability Engineer III</b>
    </td>
    <td align=center>
    <img src="https://avatars.githubusercontent.com/u/24923406?v=4" width="110" height="110"><br/>
      <a href="https://github.com/ajhenry">@ajhenry</a><br/>
      Andrew Henry<br/>
      <b> Senior Software Engineer </b>
    </td>
    <td align=center>
    <img src="https://avatars.githubusercontent.com/u/67866556?v=4" width="110" height="110"><br/>
      <a href="https://github.com/joannaakl">@joannaakl</a><br/>
      Joanna Krzek-Lubowiecka<br/>
      <b> Software Engineer III </br>
    </td>
    <td align=center>
    <img src="https://avatars.githubusercontent.com/u/22037769?v=4" width="110" height="110"><br/>
      <a href="https://github.com/dmgardiner25">@dmgardiner25</a><br/>
      David Gardiner<br/>
      <b> Software Engineer II</b>
    </td>
    <td align=center>
    <img src="https://github.com/ipc103.png?v=4" width="110" height="110"><br/>
      <a href="https://github.com/ipc103">@ipc103</a><br/>
      Ian Candy<br/>
      <b> Senior Software Engineer</b>
    </td>
   </tr>
</table>



## Development in Codespaces

<!-- TODO: Add min requirements and deployment steps -->
### Go Backend

To update the repository data using the Go backend

1. Generate a [new GitHub Token](https://github.com/settings/tokens) with the ability to read repo, read org, and  read projects scopes.
1. Set the `GRAPHQL_TOKEN` environment variable to be the value of your newly created token.
1. Run the following command from the root of the repository:
```
make build
./backend/bin/metrics
```

This will generate a new `data.json` file in the UI directory which can be imported directly as part of the static build.\

### TypeScript Backend

To update the repository data using the TypeScript backend. 

1. Generate a [new GitHub Token](https://github.com/settings/tokens) with the ability to read repo, read org, and  read projects scopes.
1. Set the `GRAPHQL_TOKEN` environment variable to be the value of your newly created token.
1. `cd backend && npm install && yarn start`. This will generate a `data.json` file in the `who-metrics-ui` directory.
1. `cd ../who-metrics-ui` and run `npm install && npm run dev` to start the server.

### UI

Run `make dev` to develop in the UI. This will:

1. Build the backend project using the steps above
1. Generate a new `data.json` file with the required data inside the frontend directory
1. Run the Next development server

