# gitignoreX
>A collection of `.gitignore` templates

这是 GitHub 的 ['.gitignore'][man] 文档模板集合。
在创建新存储库和文档时，我们使用此列表填充 GitHub.com 界面中可用的“.gitignore”模板选择器。

有关“.gitignore”文档如何工作以及如何使用它们的更多信息，
以下资源是一个很好的起点：
- The [Ignoring Files chapter][chapter] of the [Pro Git][progit] book.
- The [Ignoring Files article][help] on the GitHub Help site.
- The [gitignore(5)][man] manual page.

[man]: http://git-scm.com/docs/gitignore
[help]: https://help.github.com/articles/ignoring-files
[chapter]: https://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#_ignoring
[progit]: http://git-scm.com/book

## Folder structure

我们支持一组模板，以这种方式组织：

- T根文件夹包含常见使用的模板，以帮助人们开始使用流行的编程语言和技术。这些定义了一组有意义的规则，以帮助入门，并确保您不会将不重要的文件提交到存储库中。
- [`Global`](./Global) 包含用于不同情况的各种编辑器、工具和操作系统的模板。建议您将这些模板[添加到全局模板中](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files#configuring-ignored-files-for-all-repositories-on-your-computer)，或者将这些规则合并到项目特定的模板中，如果您想要永久使用它们的话。
- [`community`](./community) 包含其他流行语言、工具和项目的专门模板，这些模板目前不属于主流模板。当您决定采用框架或工具时，应将其添加到项目特定的模板中。

## What makes a good template?

模板应包含一组规则，以帮助 Git 存储库与特定的编程语言、框架、工具或环境配合工作。

如果无法为这种情况策划出一小组有用的规则，那么该模板就不适合放入这个集合中。

如果一个模板主要是某个软件的特定版本安装的文件列表（例如 PHP 框架），它可以位于 community 目录下。有关更多详细信息， See [versioned templates](#versioned-templates) for more details.

如果您拥有一小组规则，或者想要支持一种不广泛使用的技术，并且仍然相信这对他人有帮助，请阅读有关专门模板的部分，获取更多详细信息。

如果模板很重要且可见，请在发起拉取请求时提供详细信息。我们可能不会立即接受它，但我们可以根据兴趣将其提升到根目录中。

还请理解，我们无法列出每个曾经存在的工具。我们的目标是策划一个_最常见且有帮助的_模板集合，而不是确保我们涵盖每个可能的项目。如果我们选择不包括您的语言、工具或项目，这并不是因为它不出色。

贡献准则
我们希望您能帮助我们改进这个项目。为了保持这个集合的高质量，我们要求贡献遵守以下准则。

提供应用程序或项目主页的链接。除非它非常受欢迎，否则维护人员可能不知道或不使用您要更改的语言、框架、编辑器、应用程序或项目。

提供支持您所做更改的文档链接。提供当前、权威的文档，说明被忽略文件的情况最佳。如果没有文档支持您的更改，请尽量解释被忽略文件的用途。

解释为什么要进行更改。即使这似乎是不言自明的，也请花一两句话告诉我们为什么应该进行您的更改或添加。特别是要明确为什么这种更改适用于与适用技术一起工作的_每个人_，而不仅仅适用于您或您的团队。

请考虑您更改的范围。如果您的更改只适用于某种语言或框架，请确保将更改应用于该语言或框架的模板，而不是应用于编辑器、工具或操作系统的模板。

请每次拉取请求只修改一个模板。这有助于保持拉取请求和反馈集中在特定项目或技



If you have a small set of rules, or want to support a technology that is not
widely in use, and still believe this will be helpful to others, please read the
section about [specialized templates](#specialized-templates) for more details.

Include details when opening pull request if the template is important and visible. We
may not accept it immediately, but we can promote it to the root at a later date
based on interest.

Please also understand that we can’t list every tool that ever existed.
Our aim is to curate a collection of the _most common and helpful_ templates,
not to make sure we cover every project possible. If we choose not to
include your language, tool, or project, it’s not because it’s not awesome.

## Contributing guidelines

We’d love for you to help us improve this project. To help us keep this collection
high quality, we request that contributions adhere to the following guidelines.

- **Provide a link to the application or project’s homepage**. Unless it’s
  extremely popular, there’s a chance the maintainers don’t know about or use
  the language, framework, editor, app, or project your change applies to.

- **Provide links to documentation** supporting the change you’re making.
  Current, canonical documentation mentioning the files being ignored is best.
  If documentation isn’t available to support your change, do the best you can
  to explain what the files being ignored are for.

- **Explain why you’re making a change**. Even if it seems self-evident, please
  take a sentence or two to tell us why your change or addition should happen.
  It’s especially helpful to articulate why this change applies to _everyone_
  who works with the applicable technology, rather than just you or your team.

- **Please consider the scope of your change**. If your change is specific to a
  certain language or framework, then make sure the change is made to the
  template for that language or framework, rather than to the template for an
  editor, tool, or operating system.

- **Please only modify _one template_ per pull request**. This helps keep pull
  requests and feedback focused on a specific project or technology.

In general, the more you can do to help us understand the change you’re making,
the more likely we’ll be to accept your contribution quickly.

## Versioned templates

Some templates can change greatly between versions, and if you wish to contribute
to this repository we need to follow this specific flow:

- the template at the root should be the current supported version
- the template at the root should not have a version in the filename (i.e.
  "evergreen")
- previous versions of templates should live under `community/`
- previous versions of the template should embed the version in the filename,
  for readability

This helps ensure users get the latest version (because they'll use whatever is
at the root) but helps maintainers support older versions still in the wild.

## Specialized templates

If you have a template that you would like to contribute, but it isn't quite
mainstream, please consider adding this to the `community` directory under a
folder that best suits where it belongs.

The rules in your specialized template should be specific to the framework or
tool, and any additional templates should be mentioned in a comment in the
header of the template.

For example, this template might live at `community/DotNet/InforCRM.gitignore`:

```
# gitignore template for InforCRM (formerly SalesLogix)
# website: https://www.infor.com/product-summary/cx/infor-crm/
#
# Recommended: VisualStudio.gitignore

# Ignore model files that are auto-generated
ModelIndex.xml
ExportedFiles.xml

# Ignore deployment files
[Mm]odel/[Dd]eployment

# Force include portal SupportFiles
!Model/Portal/*/SupportFiles/[Bb]in/
!Model/Portal/PortalTemplates/*/SupportFiles/[Bb]in
```

## Contributing workflow

Here’s how we suggest you go about proposing a change to this project:

1. [Fork this project][fork] to your account.
2. [Create a branch][branch] for the change you intend to make.
3. Make your changes to your fork.
4. [Send a pull request][pr] from your fork’s branch to our `main` branch.

Using the web-based interface to make changes is fine too, and will help you
by automatically forking the project and prompting to send a pull request too.

[fork]: https://help.github.com/articles/fork-a-repo/
[branch]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository
[pr]: https://help.github.com/articles/using-pull-requests/

## License

[CC0-1.0](./LICENSE).
