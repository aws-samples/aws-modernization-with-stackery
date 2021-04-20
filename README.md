## Serverless ASP.NET Framework Modernization Workshop

This is a workshop to demonstrate how to modernize an ASP.NET REST API service, which runs on expensive, inflexible Windows servers in the cloud, into a resilient, highly scalable serverless service. The approach utilizes the [Strangler Fig Pattern](https://martinfowler.com/bliki/StranglerFigApplication.html) to modernize the application piece-by-piece rather than rewrite the entire application all at once.

## Learning Objectives

- Modernize a [.NET Framework application to .NET Core](https://dotnet.microsoft.com/learn/dotnet/what-is-dotnet-framework).
- Use the [Strangler Fig Pattern](https://martinfowler.com/bliki/StranglerFigApplication.html) to modernize one controller while leaving the rest.
- Augment the .NET Core application to run in [AWS Lambda](https://aws.amazon.com/lambda/) and serve requests from [AWS API Gateway](https://aws.amazon.com/api-gateway/) serverlessly.

## Building the Website

This page is built with Hugo, so you'll need it [installed](https://gohugo.io/getting-started/quick-start/#step-1-install-hugo)

First, clone this repo:

```bash
git clone git@github.com:aws-samples/aws-modernization-with-stackery.git
```

Ensure you've also cloned the submodules:

```bash
git submodule init
git submodule update
```

Then server the website with hugo:

```bash
hugo server
```

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.