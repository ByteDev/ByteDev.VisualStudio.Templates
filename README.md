# ByteDev.VisualStudio.Templates

Visual Studio 2022 templates for new project creation.

## Create project template

1. Edit your code project how you want it.
2. Within Visual Studio 2022 navigate to:
    - Project > Export Template... > Project template (type)
    - Select the project you want to create a template from the pulldown menu

The project template will be bundled up as a `.zip` file. Within the `.zip` file there will be:
- A template icon (`.ico` file)
- The .NET project file itself (for example `.csproj` file)
- A Visual Studio template file (`.vstemplate` file)

## Create VSIX deployment file

Wrap the finished template in a VSIX file for deployment by using the VSIX Project template.

- You will need Visual Studio SDK installed. If you don't have the SDK installed run the Visual Studio Installer, find "Visual Studio SDK" and install.
- Create an empty VSIX project: Select File > New > Project> VSIX Project 




https://learn.microsoft.com/en-us/visualstudio/extensibility/getting-started-with-the-vsix-project-template?view=vs-2022

---

## Import project template

A project template can be imported into your instance of Visual Studio.

To import a template locally copy the required `.zip` template file, for example one from `src\Templates\Projects`, to: 
`C:\Users\%USERPROFILE%\Documents\Visual Studio 2022\Templates\ProjectTemplates`

Now when you goto add a new project in Visual Studio your new imported project template type should be available for you to select.

## Remove project template

To remove a project template so it is no longer available simply goto:
`C:\Users\%USERPROFILE%\Documents\Visual Studio 2022\Templates\ProjectTemplates`

Find the `.zip` file for the project template and delete the file.

---

## Further information

- [How to create project templates](https://learn.microsoft.com/en-us/visualstudio/ide/how-to-create-project-templates?view=vs-2022)
- [How to substitute parameters in a template](https://learn.microsoft.com/en-us/visualstudio/ide/how-to-substitute-parameters-in-a-template?view=vs-2022)
- [Get started with the VSIX project template](https://learn.microsoft.com/en-us/visualstudio/extensibility/getting-started-with-the-vsix-project-template?view=vs-2022)
