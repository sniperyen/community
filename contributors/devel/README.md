# Table of Contents

这篇开发指南，适用于任何想要编写直接调用Kubernetes API的代码，或直接为 Kubernetes 项目做出贡献的人。
它假设您有一些熟悉的概念[User Guide](http://kubernetes.io/docs/user-guide/) 和 [集群操作指南](http://kubernetes.io/docs/admin/).

## 为Kubernetes项目开发和贡献代码的过程

* **贡献者指南**
  ([请从这里开始](/contributors/guide/README.md)) 了解如何为Kubernetes做出贡献

* **GitHub问题** ([issues.md](issues.md)): 新创建的问题如何分类。

* **pr 流程** ([/contributors/guide/pull-requests.md](/contributors/guide/pull-requests.md)): pr 什么时候以及为什么关闭。

* **获取最近的构建** ([getting-builds.md](getting-builds.md)): 如何获取最新版本，包括通过CI的最新版本。

* **自动化工具** ([automation.md](automation.md)): 我们的github仓库上运行的自动化。


## 设置开发环境，编码和调试

* **Development Guide** ([development.md](development.md)): 设置开发环境。

* **Testing** ([testing.md](testing.md)): 如何在开发环境中运行单元，集成和端到端测试。

* **Hunting flaky tests** ([flaky-tests.md](flaky-tests.md)): 我们的目标是99.9％覆盖测试。以下是如何多次运行测试。

* **日志约定** ([logging.md](logging.md)): Glog级别。

* **Profiling Kubernetes** ([profiling.md](profiling.md)): 如何将 pprof profileer 添加到 k8s 中。

* **如何在 k8s 中添加监控**
  ([instrumentation.md](instrumentation.md)): 如何在 k8s 中添加监控

* **编码约定** ([coding-conventions.md](../guide/coding-conventions.md)):
  为贡献者提供编码风格建议。

* **文档约定** ([how-to-doc.md](how-to-doc.md))
  为贡献者提供文档风格建议。

* **在本地运行集群** ([running-locally.md](running-locally.md)):
  用于开发的快速轻量级本地群集部署。

## 调用 Kubernetes API 进行开发

* 这篇 [REST API 文档](http://kubernetes.io/docs/reference/) 描述了 apiserver 暴露出的 REST
  API.

* **注释** ([Annotations](https://kubernetes.io/docs/concepts/overview/working-with-objects/annotations/)): are for attaching arbitrary non-identifying metadata to objects.
  Programs that automate Kubernetes objects may use annotations to store small amounts of their state.

* **API 约定** ([api-conventions.md](api-conventions.md)):
  定义了 Kubernetes API 用到的别名和资源.

* **API Client Libraries** ([client-libraries.md](client-libraries.md)):
  一组已有的 client 列表, 包含 k8s 自带的和贡献者提供的。


## 编写插件

* **验证** ([验证](http://kubernetes.io/docs/admin/authentication/)):
  当前的，以及已经在计划中的验证策略。

* **授权插件** ([授权](http://kubernetes.io/docs/admin/authorization/)):
授权适用于主 apiserver 的所有HTTP请求。本文档解释了可用的授权实现。

* **Admission 控制插件** ([admission_control](/contributors/design-proposals/api-machinery/admission_control.md))


## 创建新版本

到 [kubernetes/release](https://github.com/kubernetes/release) 仓库查看相关工具和文档。
