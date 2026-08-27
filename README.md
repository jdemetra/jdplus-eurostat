# Eurostat extensions for JDemetra+ v3

This repository has been created by a Maven archetype and contains the source code of some JDemetra+ v3 extensions.

## Developing

This project is written in Java and uses [Apache Maven](https://maven.apache.org/) as a build tool.  
It requires [Java 21 as minimum version](https://whichjdk.com/) and all its dependencies are hosted on [Maven Central](https://search.maven.org/).

The code can be built using any IDE or by just type-in the following commands in a terminal:
```shell
git clone https://github.com/jdemetra/jdplus-eurostat.git
cd jdplus-eurostat
mvn clean install
```

### Structure

```
jdplus-eurostat/
├── pom.xml                                     # Root POM (parent of all modules)
├── jdplus-eurostat-base/
│   ├── pom.xml                                 # Base aggregator
│   └── jdplus-jvsqr-base-parent/
│       ├── pom.xml                             # Base parent POM
│       ├── jdplus-jvsqr-base-api/
│       │   ├── pom.xml                         # Base API module
│       │   └── src/main/
│       └── jdplus-jvsqr-base-core/
│           ├── pom.xml                         # Base core module
│           └── src/main/
├── jdplus-eurostat-bom/
│   └── pom.xml                                 # Bill of Materials
├── jdplus-eurostat-cli/
│   └── pom.xml                                 # CLI aggregator
└── jdplus-eurostat-desktop/
    ├── pom.xml                                 # Desktop aggregator
    └── jdplus-jvsqr-desktop-plugin/
        ├── pom.xml                             # Desktop plugin module
        └── src/
            ├── main/
            │   ├── java/
            │   ├── javadoc/
            │   ├── nbm/
            │   └── resources/
            └── test/java/
```

> [!NOTE]
> `jvsqr` is the current topic used by the concrete modules. Following the naming
> convention below, this segment varies depending on the extension being developed.

### Naming

Git repositories names, Maven modules artifactId, Java modules names and Java packages names follow this naming convention:
`PREFIX-TOPIC[-STEREOTYPE[-CLASSIFIER]]`

This naming convention is enforced by the following regex pattern:
```regexp
^(jdplus)-(\w+)(?:-(base|cli|desktop|bom)(?:-(\w+))?)?$
```

## Licensing

The code of this project is licensed under the [European Union Public Licence (EUPL)](https://joinup.ec.europa.eu/page/eupl-text-11-12).
 
