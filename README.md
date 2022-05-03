# OTLoV

**O**ffline **T**emplated **Lo**gs **V**iewer - a GUI tool to help with reading diagnostic text logs. OTLoV can load a text file or a folder of text files. It creates structured, highlighted, easy to navigate view, instead of just plain text. OTLoV provides extensive text filtering capability. It also aggregates and extracts data to tabular format. All of this for different types of logs in one interface.

![OTLoV](/../../wiki/OTLoV.jpg)

OTLoV itself knows nothing about how to process specific logs. It provides a set of methods made for parsing text logs. As generic methods as possible, so that one doesn't have to redo templates with each minor logs formatting update. **Template** is what defines how to use those methods and how to match the template to specific log file/folder. This makes OTLoV easily expandable and quite flexible.

Refer to [Wiki](/../../wiki) for further information (WIP). Wiki is planned in languages: **English** and **Russian**.

>OTLoV is still in **alpha**. It can change drastically. Major rework is ongoing, ETA for the rework is not available currently. I'll make every effort possible to preserve templates, included in the package - can't do that for private templates.

## Why use it?

Diagnostic logs keep growing in size. Now, logs of >100 MB of plain text for single incident are common. That's more than the full Bible. Searching for a problem there is painful and time-consuming. Search & knowledge helps, but it's still too easy to miss things or get incomplete picture. It's like searching for a needle in haystack. That's why questions like: when, what exactly happened, what have you seen, etc. - are common in troubleshooting.

OTLoV allows you to change that. You can get immediate picture of the current state, extract diagnostic or configuration (inventory) data and more.

OTLoV is there to help people, it has no aim to replace people.

> If you came looking for timestamped logs analyzer - you are at wrong place likely. There are multiple industry-standard tools already available for that. OTLoV focuses in diagnostic logs collected by standard vendor-specific tools, which collect structured and timestamped logs.

## Development

I've worked for many years in troubleshooting-related roles, working with loads of different hardware and software. This project was started to help myself. I'm inclined to continue development of the project. Right now I'm the only developer, this might change later.

The key principles I use are:

* As simple to use as possible (point & click mostly),
* Single interface (for different types of source logs),
* Generic (adaptable),
* No bloat,
* Trust.

## Trust

I strongly believe in trust. Thus, I won't add any protection layers. No telemetry as well.

You are free to **use** this non-commercially. If you need to use this commercially and can't pay - then use it for free. But if you like the project and want it to continue evolving - please consider supporting me so that I can devote more time there.

## Privacy

OTLoV is not collecting any data. You can completely block any traffic from the app using firewall, if you wish. The only case when it could use the network is if you are loading something from a network location.

## Templates development

If you need a new template or adjust one of existing templates - you are free to do so. Welcomed, if you are willing to contribute your work to the project and include it into base package.

If you need my help with that - there are 2 ways:

* Create an issue. If I have time & consider request worth the effort - I will do it.
* Contact me directly to sign an agreement for development.

In both cases I will need source logs (preferably - multiple samples + what exactly you wish to achieve and what's important), which you can upload somewhere and give me an encrypted access. The logs will be used only for the development. No personal information will be used / extracted even if some PI is logged there. Logs will be deleted once I no longer need those for the current task, unless you explicitly give me permission to keep the logs for future development and testing.

## Support

No support is offered for free. If you want support - contact me to sign a support agreement.

Free users are welcomed to create issues and to use published documentation.

Any contributions (documentation, templates, localization) to the project are also welcomed, if you are ok that those will be merged into the base package.

## Roadmap

Some of changes that I do have on my radar currently:

* Cross-platform UI and update to .NET 6,
* CLI/GUI export of data to XML / JSON,
* Rework to a more streamlined templates,
* Scripted calculator to be able to add metrics in-place,
* Filtering / searching on all tabs,
* Relations and automatic schemes,
* Web-based version.

## System requirements

Windows Vista or later, [.NET 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework) or later v4.x.x. WPF framework is used, it's part of .NET.

## Testing

I've included a few stripped sample logs in the package. To test OTLoV:

* Run **OTLoV.exe**.
* Click "**Load**" button or `CTRL + L`, navigate to Test folder and select one or more files / folders there. You can use `shift + mouse click` or `ctrl + mouse click` to select multiple items. Note, that Filtering samples won't be loaded unless you select the files explicitly.
* Wait for loading to complete.
* Explore the source and OTLoV. Follow Filtering readme.

## License

See [LICENSE-EN.md](LICENSE-EN.md) for English license text or [LICENSE-RU.md](LICENSE-RU.md) for Russian text.
