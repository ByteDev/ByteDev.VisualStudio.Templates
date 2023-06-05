# ByteDev.VisualStudio.Templates

Visual Studio 2022 templates for new project/file creation.

## Create project template

To create a Visual Studio project template:

1. Edit your code project how you want it.
2. Within Visual Studio 2022 navigate to:
    - Project > Export Template... > Project template (type)
    - Select the project you want to create a template from the pulldown menu

The project template will be bundled up as a `.zip` file. Within the `.zip` file there will be:
- A template icon (`.ico` file)
- The .NET project file itself (for example `.csproj` file)
- A Visual Studio template file (`.vstemplate` file)

## Manually import project template

A project template can be imported into your instance of Visual Studio.

To import a template locally copy the required `.zip` template file to: 
`C:\Users\%USERPROFILE%\Documents\Visual Studio 2022\Templates\ProjectTemplates`

Now when you goto add a new project in Visual Studio your new imported project template type should be available for you to select.

## Manually remove project template

To remove a project template so it is no longer available simply:
- Navigate to: `C:\Users\%USERPROFILE%\Documents\Visual Studio 2022\Templates\ProjectTemplates`
- Find the `.zip` file for the project template and delete it.

---

## Create VSIX deployment file

The template `.zip` file can be wrapped in a VSIX file for easy deployment as a Visual Studio extension.

Firstly you will need Visual Studio SDK installed. If you don't have the SDK installed run the Visual Studio Installer, find "Visual Studio SDK" and install.

To wrap the `.zip` file in a VSIX deployment file:

- Create an empty VSIX project in Visual Studio: 
    - Select File > New > Project> VSIX Project
- Copy the template `.zip` file to the root of the new VSIX project
    - Set the `.zip` file's "Copy to Output Directory" setting to `Copy Always`
- Open the `.vsixmanifest` file in Visual Studio. This should open a dialog box
- In the Metadata section:
    - Set the Product Name
    - Set the Product ID to the same as Product Name with a `-1` suffix
    - Set the Author
    - Set the Description
- In the Assets section:
    - Add a "Microsoft.VisualStudio.ProjectTemplate" type and set its path to the name of the .zip file
- Save and close the file
- Build the VSIX project
- The new `.vsix` can now be found in the project's `bin` folder
- Run this `.vsix` file to install the project template as a Visual Studio extension

To manage/remove the project template extension within Visual Studio navigate to:
Extensions > Manage Extensions > Installed (section)

---

## Further information

- [How to create project templates](https://learn.microsoft.com/en-us/visualstudio/ide/how-to-create-project-templates?view=vs-2022)
- [How to substitute parameters in a template](https://learn.microsoft.com/en-us/visualstudio/ide/how-to-substitute-parameters-in-a-template?view=vs-2022)
- [Get started with the VSIX project template](https://learn.microsoft.com/en-us/visualstudio/extensibility/getting-started-with-the-vsix-project-template?view=vs-2022)
