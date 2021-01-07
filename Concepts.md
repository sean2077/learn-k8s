- [K8S 概念](#k8s-%E6%A6%82%E5%BF%B5)
  - [概述](#%E6%A6%82%E8%BF%B0)
    - [Kubernetes 是什么？](#kubernetes-%E6%98%AF%E4%BB%80%E4%B9%88)
    - [Kubernetes 组件](#kubernetes-%E7%BB%84%E4%BB%B6)
    - [Kubernetes API](#kubernetes-api)
    - [使用 Kubernetes 对象](#%E4%BD%BF%E7%94%A8-kubernetes-%E5%AF%B9%E8%B1%A1)
  - [Kubernetes 架构](#kubernetes-%E6%9E%B6%E6%9E%84)
    - [节点](#%E8%8A%82%E7%82%B9)
    - [控制面到节点通信](#%E6%8E%A7%E5%88%B6%E9%9D%A2%E5%88%B0%E8%8A%82%E7%82%B9%E9%80%9A%E4%BF%A1)
    - [控制器](#%E6%8E%A7%E5%88%B6%E5%99%A8)
    - [云控制器管理器的基础概念](#%E4%BA%91%E6%8E%A7%E5%88%B6%E5%99%A8%E7%AE%A1%E7%90%86%E5%99%A8%E7%9A%84%E5%9F%BA%E7%A1%80%E6%A6%82%E5%BF%B5)
  - [容器](#%E5%AE%B9%E5%99%A8)
  - [工作负载](#%E5%B7%A5%E4%BD%9C%E8%B4%9F%E8%BD%BD)
    - [Pods](#pods)
      - [Pod 生命周期](#pod-%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F)
      - [Init 容器](#init-%E5%AE%B9%E5%99%A8)
      - [Pod 拓扑分布约束](#pod-%E6%8B%93%E6%89%91%E5%88%86%E5%B8%83%E7%BA%A6%E6%9D%9F)
      - [干扰（Disruptions）](#%E5%B9%B2%E6%89%B0disruptions)
      - [临时容器](#%E4%B8%B4%E6%97%B6%E5%AE%B9%E5%99%A8)
    - [工作负载资源](#%E5%B7%A5%E4%BD%9C%E8%B4%9F%E8%BD%BD%E8%B5%84%E6%BA%90)
      - [ReplicaSet](#replicaset)
      - [Deployments](#deployments)
      - [StatefulSets](#statefulsets)
      - [DaemonSet](#daemonset)
      - [Jobs](#jobs)
      - [垃圾收集](#%E5%9E%83%E5%9C%BE%E6%94%B6%E9%9B%86)
      - [已完成资源的 TTL 控制器](#%E5%B7%B2%E5%AE%8C%E6%88%90%E8%B5%84%E6%BA%90%E7%9A%84-ttl-%E6%8E%A7%E5%88%B6%E5%99%A8)
      - [CronJob](#cronjob)
      - [ReplicationController](#replicationcontroller)
  - [服务、负载均衡和联网](#%E6%9C%8D%E5%8A%A1%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1%E5%92%8C%E8%81%94%E7%BD%91)
  - [存储](#%E5%AD%98%E5%82%A8)
  - [配置](#%E9%85%8D%E7%BD%AE)
  - [安全](#%E5%AE%89%E5%85%A8)
  - [策略](#%E7%AD%96%E7%95%A5)
  - [调度和驱逐 (Scheduling and Eviction)](#%E8%B0%83%E5%BA%A6%E5%92%8C%E9%A9%B1%E9%80%90-scheduling-and-eviction)
  - [集群管理](#%E9%9B%86%E7%BE%A4%E7%AE%A1%E7%90%86)
  - [扩展 Kubernetes](#%E6%89%A9%E5%B1%95-kubernetes)

# K8S 概念

## [概述](https://kubernetes.io/zh/docs/concepts/overview/)

获得 Kubernetes 及其构件的高层次概要。

#### [Kubernetes 是什么？](https://kubernetes.io/zh/docs/concepts/overview/what-is-kubernetes/)

Kubernetes 是一个可移植的，可扩展的开源平台，用于管理容器化的工作负载和服务，方便了声明式配置和自动化。它拥有一个庞大且快速增长的生态系统。Kubernetes 的服务，支持和工具广泛可用。

#### [Kubernetes 组件](https://kubernetes.io/zh/docs/concepts/overview/components/)

Kubernetes 集群由代表控制平面的组件和一组称为节点的机器组成。

#### [Kubernetes API](https://kubernetes.io/zh/docs/concepts/overview/kubernetes-api/)

Kubernetes API 使你可以查询和操纵 Kubernetes 中对象的状态。 Kubernetes 控制平面的核心是 API 服务器和它暴露的 HTTP API。 用户、集群的不同部分以及外部组件都通过 API 服务器相互通信。

#### [使用 Kubernetes 对象](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/)

Kubernetes 对象是 Kubernetes 系统中的持久性实体。Kubernetes 使用这些实体表示您的集群状态。了解 Kubernetes 对象模型以及如何使用这些对象。

## [Kubernetes 架构](https://kubernetes.io/zh/docs/concepts/architecture/)

Kubernetes 背后的架构概念。

#### [节点](https://kubernetes.io/zh/docs/concepts/architecture/nodes/)

#### [控制面到节点通信](https://kubernetes.io/zh/docs/concepts/architecture/control-plane-node-communication/)

#### [控制器](https://kubernetes.io/zh/docs/concepts/architecture/controller/)

#### [云控制器管理器的基础概念](https://kubernetes.io/zh/docs/concepts/architecture/cloud-controller/)

## [容器](https://kubernetes.io/zh/docs/concepts/containers/)

打包应用及其运行依赖环境的技术。

## [工作负载](https://kubernetes.io/zh/docs/concepts/workloads/)

理解 Pods，Kubernetes 中可部署的最小计算对象，以及辅助它运行它们的高层抽象对象。

### [Pods](https://kubernetes.io/zh/docs/concepts/workloads/pods/)

Pod: 运行在集群上的一组容器，是 kubernetes 中最小的可部署计算单位。

**内部容器特点**

- 有确定的生命周期的

- 共享内存/网络资源
- 共享容器启动规范
- 内容协同、共同调度且共享上下文（Linux 命名空间，控制组及其他容器隔离方面）

注：从官网描述来看，一个 Pod 的所有容器应该在同一个物理机或虚拟机上运行。

> The containers in a Pod are automatically co-located and co-scheduled on the same physical or virtual machine in the cluster.

Pod 除了 app 容器外还可有初始化容器，初始化容器在 app 容器启动之前执行。

**运行方式**

- 一个 pod 运行一个容器（one-container-per-Pod），最常用
- 一个 pod 运行多个协同的容器

**创建 Pod**

通常通过负载资源创建 Pod

Workload resources: 通过 controller 管理一组 Pod。内置负载资源包括：

- Deployment 和 ReplicaSet
- StatefulSet
- DaemonSet
- Job 和 CronJob

支持自定义负载资源。

Controller 通常通过`pod template`创建 Pods。

**更新和替换 Pod**

通常，我们需要通过 Controller 间接管理 Pod，修改 pod template 然后交由 controller 去操作。一般而言，pod template 的修改不会对现存的 pod 造成影响，而是会新建基于当前模板的 pods。但这种行为也取决于负载资源的[更新策略](https://kubernetes.io/docs/tutorials/stateful-application/basic-stateful-set/#updating-statefulsets)。

kubernetes 也支持直接对 Pod 进行更新操作，如 patch，replace 操作，但存在一定限制。

**资源共享和通信**

在同一个 Pod 内，所有容器共享一个 IP 地址和端口空间，并且可以通过 `localhost` 发现对方。 他们也能通过如 SystemV 信号量或 POSIX 共享内存这类标准的进程间通信方式互相通信。 不同 Pod 中的容器的 IP 地址互不相同，没有 [特殊配置](https://kubernetes.io/zh/docs/concepts/policy/pod-security-policy/) 就不能使用 IPC 进行通信。 如果某容器希望与运行于其他 Pod 中的容器通信，可以通过 IP 联网的方式实现。

Pod 中的容器所看到的系统主机名与为 Pod 配置的 `name` 属性值相同。

**容器的特权模式**

Pod 中的任何容器都可以使用容器规约中的 [安全性上下文](https://kubernetes.io/zh/docs/tasks/configure-pod-container/security-context/)中的 `privileged` 参数启用特权模式。 这对于想要使用使用操作系统管理权能（Capabilities，如操纵网络堆栈和访问设备） 的容器很有用。 容器内的进程几乎可以获得与容器外的进程相同的特权。

> **说明：** 你的[容器运行时](https://kubernetes.io/zh/docs/setup/production-environment/container-runtimes)必须支持 特权容器的概念才能使用这一配置。

**静态 Pod**

_静态 Pod（Static Pod）_ 直接由特定节点上的 `kubelet` 守护进程管理， 不需要[API 服务器](https://kubernetes.io/zh/docs/reference/command-line-tools-reference/kube-apiserver/)看到它们。 尽管大多数 Pod 都是通过控制面（例如，[Deployment](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/)） 来管理的，对于静态 Pod 而言，`kubelet` 直接监控每个 Pod，并在其失效时重启之。

静态 Pod 通常绑定到某个节点上的 [kubelet](https://kubernetes.io/docs/reference/generated/kubelet)。 其主要用途是运行自托管的控制面。 在自托管场景中，使用 `kubelet` 来管理各个独立的 [控制面组件](https://kubernetes.io/zh/docs/concepts/overview/components/#control-plane-components)。

`kubelet` 自动尝试为每个静态 Pod 在 Kubernetes API 服务器上创建一个 [镜像 Pod](https://kubernetes.io/zh/docs/reference/glossary/?all=true#term-mirror-pod)。 这意味着在节点上运行的 Pod 在 API 服务器上是可见的，但不可以通过 API 服务器来控制。

#### Pod 生命周期

**Pod 阶段**

Pod 遵循一个预定义的生命周期，起始于 `Pending` [阶段](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-phase)，如果至少 其中有一个主要容器正常启动，则进入 `Running`，之后取决于 Pod 中是否有容器以 失败状态结束而进入 `Succeeded` 或者 `Failed` 阶段。

在 Pod 运行期间，`kubelet` 能够重启容器以处理一些失效场景。 在 Pod 内部，Kubernetes 跟踪不同容器的[状态](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#container-states) 并确定使 Pod 重新变得健康所需要采取的动作。

在 Kubernetes API 中，Pod 包含规约部分和实际状态部分。 Pod 对象的状态包含了一组 [Pod 状况（Conditions）](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-conditions)。 如果应用需要的话，你也可以向其中注入[自定义的就绪性信息](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-readiness-gate)。

Pod 在其生命周期中只会被[调度](https://kubernetes.io/zh/docs/concepts/scheduling-eviction/)一次。 一旦 Pod 被调度（分派）到某个节点，Pod 会一直在该节点运行，直到 Pod 停止或者 被[终止](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-termination)。

Pod 的 `status` 字段是一个 [PodStatus](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#podstatus-v1-core) 对象，其中包含一个 `phase` 字段。

Pod 的阶段（Phase）是 Pod 在其生命周期中所处位置的简单宏观概述。 该阶段并不是对容器或 Pod 状态的综合汇总，也不是为了成为完整的状态机。

Pod 阶段的数量和含义是严格定义的。 除了本文档中列举的内容外，不应该再假定 Pod 有其他的 `phase` 值。

| 取值                | 描述                                                                                                                          |
| :------------------ | :---------------------------------------------------------------------------------------------------------------------------- |
| `Pending`（悬决）   | Pod 已被 Kubernetes 系统接受，但有一个或者多个容器尚未创建亦未运行。此阶段包括等待 Pod 被调度的时间和通过网络下载镜像的时间， |
| `Running`（运行中） | Pod 已经绑定到了某个节点，Pod 中所有的容器都已被创建。至少有一个容器仍在运行，或者正处于启动或重启状态。                      |
| `Succeeded`（成功） | Pod 中的所有容器都已成功终止，并且不会再重启。                                                                                |
| `Failed`（失败）    | Pod 中的所有容器都已终止，并且至少有一个容器是因为失败终止。也就是说，容器以非 0 状态退出或者被系统终止。                     |
| `Unknown`（未知）   | 因为某些原因无法取得 Pod 的状态。这种情况通常是因为与 Pod 所在主机通信失败。                                                  |

如果某节点死掉或者与集群中其他节点失联，Kubernetes 会实施一种策略，将失去的节点上运行的所有 Pod 的 `phase` 设置为 `Failed`。

**容器状态**

Kubernetes 会跟踪 Pod 中每个容器的状态，就像它跟踪 Pod 总体上的[阶段](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-phase)一样。 你可以使用[容器生命周期回调](https://kubernetes.io/zh/docs/concepts/containers/container-lifecycle-hooks/) 来在容器生命周期中的特定时间点触发事件。

一旦[调度器](https://kubernetes.io/docs/reference/generated/kube-scheduler/)将 Pod 分派给某个节点，`kubelet` 就通过 [容器运行时](https://kubernetes.io/zh/docs/setup/production-environment/container-runtimes) 开始为 Pod 创建容器。 容器的状态有三种：`Waiting`（等待）、`Running`（运行中）和 `Terminated`（已终止）。

要检查 Pod 中容器的状态，你可以使用 `kubectl describe pod <pod 名称>`。 其输出中包含 Pod 中每个容器的状态。

每种状态都有特定的含义：

`Waiting` （等待）

如果容器并不处在 `Running` 或 `Terminated` 状态之一，它就处在 `Waiting` 状态。 处于 `Waiting` 状态的容器仍在运行它完成启动所需要的操作：例如，从某个容器镜像 仓库拉取容器镜像，或者向容器应用 [Secret](https://kubernetes.io/zh/docs/concepts/configuration/secret/) 数据等等。 当你使用 `kubectl` 来查询包含 `Waiting` 状态的容器的 Pod 时，你也会看到一个 Reason 字段，其中给出了容器处于等待状态的原因。

`Running`（运行中）

`Running` 状态表明容器正在执行状态并且没有问题发生。 如果配置了 `postStart` 回调，那么该回调已经执行且已完成。 如果你使用 `kubectl` 来查询包含 `Running` 状态的容器的 Pod 时，你也会看到 关于容器进入 `Running` 状态的信息。

`Terminated`（已终止）

处于 `Terminated` 状态的容器已经开始执行并且或者正常结束或者因为某些原因失败。 如果你使用 `kubectl` 来查询包含 `Terminated` 状态的容器的 Pod 时，你会看到 容器进入此状态的原因、退出代码以及容器执行期间的起止时间。如果容器配置了 `preStop` 回调，则该回调会在容器进入 `Terminated` 状态之前执行。

**容器重启策略**

Pod 的 `spec` 中包含一个 `restartPolicy` 字段，其可能取值包括 Always、OnFailure 和 Never。默认值是 Always。

`restartPolicy` 适用于 Pod 中的所有容器。`restartPolicy` 仅针对同一节点上 `kubelet` 的容器重启动作。当 Pod 中的容器退出时，`kubelet` 会按指数回退 方式计算重启的延迟（10s、20s、40s、...），其最长延迟为 5 分钟。 一旦某容器执行了 10 分钟并且没有出现问题，`kubelet` 对该容器的重启回退计时器执行 重置操作。

**Pod 状况**

Pod 有一个 PodStatus 对象，其中包含一个 [PodConditions](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#podcondition-v1-core) 数组。Pod 可能通过也可能未通过其中的一些状况测试。

- `PodScheduled`：Pod 已经被调度到某节点；
- `ContainersReady`：Pod 中所有容器都已就绪；
- `Initialized`：所有的 [Init 容器](https://kubernetes.io/zh/docs/concepts/workloads/pods/init-containers/) 都已成功启动；
- `Ready`：Pod 可以为请求提供服务，并且应该被添加到对应服务的负载均衡池中。

| 字段名称             | 描述                                                                 |
| :------------------- | :------------------------------------------------------------------- |
| `type`               | Pod 状况的名称                                                       |
| `status`             | 表明该状况是否适用，可能的取值有 "`True`", "`False`" 或 "`Unknown`"  |
| `lastProbeTime`      | 上次探测 Pod 状况时的时间戳                                          |
| `lastTransitionTime` | Pod 上次从一种状态转换到另一种状态时的时间戳                         |
| `reason`             | 机器可读的、驼峰编码（UpperCamelCase）的文字，表述上次状况变化的原因 |
| `message`            | 人类可读的消息，给出上次状态转换的详细信息                           |

**Pod 就绪态**

**FEATURE STATE:** `Kubernetes v1.14 [stable]`

你的应用可以向 PodStatus 中注入额外的反馈或者信号：_Pod Readiness（Pod 就绪态）_。 要使用这一特性，可以设置 Pod 规约中的 `readinessGates` 列表，为 kubelet 提供一组额外的状况供其评估 Pod 就绪态时使用。

就绪态门控基于 Pod 的 `status.conditions` 字段的当前值来做决定。 如果 Kubernetes 无法在 `status.conditions` 字段中找到某状况，则该状况的 状态值默认为 "`False`"。

这里是一个例子：

```yaml
kind: Pod
---
spec:
  readinessGates:
    - conditionType: "www.example.com/feature-1"
status:
  conditions:
    - type: Ready # 内置的 Pod 状况
      status: "False"
      lastProbeTime: null
      lastTransitionTime: 2018-01-01T00:00:00Z
    - type: "www.example.com/feature-1" # 额外的 Pod 状况
      status: "False"
      lastProbeTime: null
      lastTransitionTime: 2018-01-01T00:00:00Z
  containerStatuses:
    - containerID: docker://abcd...
      ready: true
```

你所添加的 Pod 状况名称必须满足 Kubernetes [标签键名格式](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/labels/#syntax-and-character-set)。

命令 `kubectl patch` 不支持修改对象的状态。 如果需要设置 Pod 的 `status.conditions`，应用或者 [Operators](https://kubernetes.io/zh/docs/concepts/extend-kubernetes/operator/) 需要使用 `PATCH` 操作。 你可以使用 [Kubernetes 客户端库](https://kubernetes.io/zh/docs/reference/using-api/client-libraries/) 之一来编写代码，针对 Pod 就绪态设置定制的 Pod 状况。

对于使用定制状况的 Pod 而言，只有当下面的陈述都适用时，该 Pod 才会被评估为就绪：

- Pod 中所有容器都已就绪；
- `readinessGates` 中的所有状况都为 `True` 值。

当 Pod 的容器都已就绪，但至少一个定制状况没有取值或者取值为 `False`， `kubelet` 将 Pod 的[状况](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#pod-conditions)设置为 `ContainersReady`。

**容器探针**

[Probe](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#probe-v1-core) 是由 [kubelet](https://kubernetes.io/zh/docs/reference/command-line-tools-reference/kubelet/) 对容器执行的定期诊断。 要执行诊断，kubelet 调用由容器实现的 [Handler](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#handler-v1-core) （处理程序）。有三种类型的处理程序：

- [ExecAction](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#execaction-v1-core)： 在容器内执行指定命令。如果命令退出时返回码为 0 则认为诊断成功。
- [TCPSocketAction](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#tcpsocketaction-v1-core)： 对容器的 IP 地址上的指定端口执行 TCP 检查。如果端口打开，则诊断被认为是成功的。
- [HTTPGetAction](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#httpgetaction-v1-core)： 对容器的 IP 地址上指定端口和路径执行 HTTP Get 请求。如果响应的状态码大于等于 200 且小于 400，则诊断被认为是成功的。

每次探测都将获得以下三种结果之一：

- `Success`（成功）：容器通过了诊断。
- `Failure`（失败）：容器未通过诊断。
- `Unknown`（未知）：诊断失败，因此不会采取任何行动。

针对运行中的容器，`kubelet` 可以选择是否执行以下三种探针，以及如何针对探测结果作出反应：

- `livenessProbe`：指示容器是否正在运行。如果存活态探测失败，则 kubelet 会杀死容器， 并且容器将根据其[重启策略](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy)决定未来。如果容器不提供存活探针， 则默认状态为 `Success`。
- `readinessProbe`：指示容器是否准备好为请求提供服务。如果就绪态探测失败， 端点控制器将从与 Pod 匹配的所有服务的端点列表中删除该 Pod 的 IP 地址。 初始延迟之前的就绪态的状态值默认为 `Failure`。 如果容器不提供就绪态探针，则默认状态为 `Success`。
- `startupProbe`: 指示容器中的应用是否已经启动。如果提供了启动探针，则所有其他探针都会被 禁用，直到此探针成功为止。如果启动探测失败，`kubelet` 将杀死容器，而容器依其 [重启策略](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy)进行重启。 如果容器没有提供启动探测，则默认状态为 `Success`。

如欲了解如何设置存活态、就绪态和启动探针的进一步细节，可以参阅 [配置存活态、就绪态和启动探针](https://kubernetes.io/zh/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)。

何时该使用存活态探针?

**FEATURE STATE:** `Kubernetes v1.0 [stable]`

如果容器中的进程能够在遇到问题或不健康的情况下自行崩溃，则不一定需要存活态探针; `kubelet` 将根据 Pod 的`restartPolicy` 自动执行修复操作。

如果你希望容器在探测失败时被杀死并重新启动，那么请指定一个存活态探针， 并指定`restartPolicy` 为 "`Always`" 或 "`OnFailure`"。

何时该使用就绪态探针?

**FEATURE STATE:** `Kubernetes v1.0 [stable]`

如果要仅在探测成功时才开始向 Pod 发送请求流量，请指定就绪态探针。 在这种情况下，就绪态探针可能与存活态探针相同，但是规约中的就绪态探针的存在意味着 Pod 将在启动阶段不接收任何数据，并且只有在探针探测成功后才开始接收数据。

如果你的容器需要加载大规模的数据、配置文件或者在启动期间执行迁移操作，可以添加一个 就绪态探针。

如果你希望容器能够自行进入维护状态，也可以指定一个就绪态探针，检查某个特定于 就绪态的因此不同于存活态探测的端点。

> **说明：** 请注意，如果你只是想在 Pod 被删除时能够排空请求，则不一定需要使用就绪态探针； 在删除 Pod 时，Pod 会自动将自身置于未就绪状态，无论就绪态探针是否存在。 等待 Pod 中的容器停止期间，Pod 会一直处于未就绪状态。

何时该使用启动探针？

**FEATURE STATE:** `Kubernetes v1.18 [beta]`

对于所包含的容器需要较长时间才能启动就绪的 Pod 而言，启动探针是有用的。 你不再需要配置一个较长的存活态探测时间间隔，只需要设置另一个独立的配置选定， 对启动期间的容器执行探测，从而允许使用远远超出存活态时间间隔所允许的时长。

如果你的容器启动时间通常超出 `initialDelaySeconds + failureThreshold × periodSeconds` 总值，你应该设置一个启动探测，对存活态探针所使用的同一端点执行检查。 `periodSeconds` 的默认值是 30 秒。你应该将其 `failureThreshold` 设置得足够高， 以便容器有充足的时间完成启动，并且避免更改存活态探针所使用的默认值。 这一设置有助于减少死锁状况的发生。

**强制终止 Pod**

> **注意：** 对于某些工作负载及其 Pod 而言，强制删除很可能会带来某种破坏。

默认情况下，所有的删除操作都会附有 30 秒钟的宽限期限。 `kubectl delete` 命令支持 `--grace-period=<seconds>` 选项，允许你重载默认值， 设定自己希望的期限值。

将宽限期限强制设置为 `0` 意味着立即从 API 服务器删除 Pod。 如果 Pod 仍然运行于某节点上，强制删除操作会触发 `kubelet` 立即执行清理操作。

> **说明：** 你必须在设置 `--grace-period=0` 的同时额外设置 `--force` 参数才能发起强制删除请求。

执行强制删除操作时，API 服务器不再等待来自 `kubelet` 的、关于 Pod 已经在原来运行的节点上终止执行的确认消息。 API 服务器直接删除 Pod 对象，这样新的与之同名的 Pod 即可以被创建。 在节点侧，被设置为立即终止的 Pod 仍然会在被强行杀死之前获得一点点的宽限时间。

如果你需要强制删除 StatefulSet 的 Pod，请参阅 [从 StatefulSet 中删除 Pod](https://kubernetes.io/zh/docs/tasks/run-application/force-delete-stateful-set-pod/) 的任务文档。

**失效 Pod 的垃圾收集**

对于已失败的 Pod 而言，对应的 API 对象仍然会保留在集群的 API 服务器上，直到 用户或者[控制器](https://kubernetes.io/zh/docs/concepts/architecture/controller/)进程显式地 将其删除。

控制面组件会在 Pod 个数超出所配置的阈值 （根据 `kube-controller-manager` 的 `terminated-pod-gc-threshold` 设置）时 删除已终止的 Pod（阶段值为 `Succeeded` 或 `Failed`）。 这一行为会避免随着时间演进不断创建和终止 Pod 而引起的资源泄露问题。

#### Init 容器

Init 容器是一种特殊容器，在 [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/) 内的应用容器启动之前运行。Init 容器可以包括一些应用镜像中不存在的实用工具和安装脚本。

每个 [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/) 中可以包含多个容器， 应用运行在这些容器里面，同时 Pod 也可以有一个或多个先于应用容器启动的 Init 容器。

Init 容器与普通的容器非常像，除了如下两点：

- 它们总是运行到完成。
- 每个都必须在下一个启动之前成功完成。

如果 Pod 的 Init 容器失败，kubelet 会不断地重启该 Init 容器直到该容器成功为止。 然而，如果 Pod 对应的 `restartPolicy` 值为 "Never"，Kubernetes 不会重新启动 Pod。

为 Pod 设置 Init 容器需要在 Pod 的 `spec` 中添加 `initContainers` 字段， 该字段以 [Container](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.20/#container-v1-core) 类型对象数组的形式组织，和应用的 `containers` 数组同级相邻。 Init 容器的状态在 `status.initContainerStatuses` 字段中以容器状态数组的格式返回 （类似 `status.containerStatuses` 字段）。

Init 容器支持应用容器的全部字段和特性，包括资源限制、数据卷和安全设置。 然而，Init 容器对资源请求和限制的处理稍有不同，在下面[资源](https://kubernetes.io/zh/docs/concepts/workloads/pods/init-containers/#resources)节有说明。

同时 Init 容器不支持 `lifecycle`、`livenessProbe`、`readinessProbe` 和 `startupProbe`， 因为它们必须在 Pod 就绪之前运行完成。

如果为一个 Pod 指定了多个 Init 容器，这些容器会按顺序逐个运行。 每个 Init 容器必须运行成功，下一个才能够运行。当所有的 Init 容器运行完成时， Kubernetes 才会为 Pod 初始化应用容器并像平常一样运行。

#### Pod 拓扑分布约束

**FEATURE STATE:** `Kubernetes v1.19 [stable]`

你可以使用 _拓扑分布约束（Topology Spread Constraints）_ 来控制 [Pods](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/) 在集群内故障域 之间的分布，例如区域（Region）、可用区（Zone）、节点和其他用户自定义拓扑域。 这样做有助于实现高可用并提升资源利用率。

> **说明：** 在 v1.19 之前的 Kubernetes 版本中，如果要使用 Pod 拓扑扩展约束，你必须在 [API 服务器](https://kubernetes.io/zh/docs/concepts/overview/components/#kube-apiserver) 和[调度器](https://kubernetes.io/zh/docs/reference/command-line-tools-reference/kube-scheduler/) 中启用 `EvenPodsSpread` [特性门控](https://kubernetes.io/zh/docs/reference/command-line-tools-reference/feature-gates/)。

#### 干扰（Disruptions）

#### 临时容器

种特殊的容器，该容器在现有 [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/) 中临时运行，以便完成用户发起的操作，例如故障排查。 你会使用临时容器来检查服务，而不是用它来构建应用程序。

### [工作负载资源](https://kubernetes.io/zh/docs/concepts/workloads/controllers/)

#### [ReplicaSet](https://kubernetes.io/zh/docs/concepts/workloads/controllers/replicaset/)

#### [Deployments](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/)

#### [StatefulSets](https://kubernetes.io/zh/docs/concepts/workloads/controllers/statefulset/)

#### [DaemonSet](https://kubernetes.io/zh/docs/concepts/workloads/controllers/daemonset/)

#### [Jobs](https://kubernetes.io/zh/docs/concepts/workloads/controllers/job/)

#### [垃圾收集](https://kubernetes.io/zh/docs/concepts/workloads/controllers/garbage-collection/)

#### [已完成资源的 TTL 控制器](https://kubernetes.io/zh/docs/concepts/workloads/controllers/ttlafterfinished/)

#### [CronJob](https://kubernetes.io/zh/docs/concepts/workloads/controllers/cron-jobs/)

#### [ReplicationController](https://kubernetes.io/zh/docs/concepts/workloads/controllers/replicationcontroller/)

## [服务、负载均衡和联网](https://kubernetes.io/zh/docs/concepts/services-networking/)

Kubernetes 网络背后的概念和资源。

## [存储](https://kubernetes.io/zh/docs/concepts/storage/)

为集群中的 Pods 提供长期和临时存储的方法。

## [配置](https://kubernetes.io/zh/docs/concepts/configuration/)

Kubernetes 为配置 Pods 提供的资源。

## [安全](https://kubernetes.io/zh/docs/concepts/security/)

确保云原生工作负载安全的一组概念。

## [策略](https://kubernetes.io/zh/docs/concepts/policy/)

可配置的、可应用到一组资源的策略。

## [调度和驱逐 (Scheduling and Eviction)](https://kubernetes.io/zh/docs/concepts/scheduling-eviction/)

在 Kubernetes 中，调度 (Scheduling) 指的是确保 Pods 匹配到合适的节点，以便 kubelet 能够运行它们。驱逐 (Eviction) 是在资源匮乏的节点上，主动让一个或多个 Pods 失效的过程。

## [集群管理](https://kubernetes.io/zh/docs/concepts/cluster-administration/)

关于创建和管理 Kubernetes 集群的底层细节。

## [扩展 Kubernetes](https://kubernetes.io/zh/docs/concepts/extend-kubernetes/)

改变你的 Kubernetes 集群的行为的若干方法。
