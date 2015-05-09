# Heroku Buildpack For .Net

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for building .Net applications.

It supports [ASP.NET 5](http://www.asp.net/vnext/overview/aspnet-vnext/aspnet-5-overview) applications using [`project.json`](https://github.com/aspnet/Home/wiki/Project.json-file) files and the [DNU package manager](https://github.com/aspnet/Home/wiki/Package-Manager).

[Mono](http://www.mono-project.com/) is bundled for runtime execution.

## Usage

Example usage:

    $ heroku create --buildpack http://github.com/yngndrw/dotnet-buildpack.git
    $ git push heroku master

The buildpack will detect your application as ASP.NET 5 if it has a `project.json`. If the source code you want to build contains multiple `project.json` files, you can use a [`.deployment`](https://github.com/projectkudu/kudu/wiki/Customizing-deployments) or set a `$PROJECT` config var to control which one is built.
