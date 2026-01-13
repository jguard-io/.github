<p align="center">
  <a href="https://jguard.io">
    <img src="https://jguard.io/img/jguard-logo-transparent-background.png" alt="jGuard" width="400">
  </a>
</p>

<p align="center">
  <strong>Capability-Based Security Framework for the JVM</strong>
</p>

<p align="center">
  <a href="https://github.com/jguard-io/jguard/actions/workflows/ci.yml">
    <img src="https://github.com/jguard-io/jguard/actions/workflows/ci.yml/badge.svg" alt="Build Status">
  </a>
  <a href="https://central.sonatype.com/search?q=io.jguard">
    <img src="https://img.shields.io/maven-central/v/io.jguard/jguard-core?label=Maven%20Central" alt="Maven Central">
  </a>
  <a href="https://plugins.gradle.org/plugin/io.jguard.policy">
    <img src="https://img.shields.io/gradle-plugin-portal/v/io.jguard.policy?label=Gradle%20Plugin" alt="Gradle Plugin">
  </a>
  <a href="https://jguard.io">
    <img src="https://img.shields.io/badge/docs-jguard.io-blue" alt="Documentation">
  </a>
</p>

---

jGuard enables JVM applications to execute untrusted code—plugins, extensions, and embedded automation—with explicit, least-privilege access controls.

Built for JDK 21+ in the post-SecurityManager era.

## Example Policy

```text
security module com.example.myapp {
    entitle com.example.myapp.http.. to network.outbound;
    entitle com.example.myapp.io..   to fs.read(data, "**");
    entitle com.example.myapp..      to threads.create;
}
```

## Quick Start

```groovy
plugins {
    id "io.jguard.policy" version "0.2.0"
}
```

```bash
./gradlew runWithAgent
```

## Resources

| | |
|---|---|
| [Documentation](https://jguard.io) | Getting started, policy reference, tutorials |
| [GitHub](https://github.com/jguard-io/jguard) | Source code and issues |
| [Maven Central](https://central.sonatype.com/search?q=io.jguard) | Released artifacts |
| [Gradle Plugin](https://plugins.gradle.org/plugin/io.jguard.policy) | Build integration |

## Community

We welcome contributions! Please read our community guidelines:

- [Contributing Guide](https://jguard.io/docs/community/contributing) - How to contribute code and documentation
- [Code of Conduct](https://jguard.io/docs/community/code-of-conduct) - Expected behavior and community standards
- [Governance](https://jguard.io/docs/community/governance) - Project decision-making process
- [Security Policy](https://jguard.io/docs/community/security) - How to report vulnerabilities

## License

Apache 2.0
