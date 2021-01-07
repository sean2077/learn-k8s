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

ReplicaSet 的目的是维护一组在任何时候都处于运行状态的 Pod 副本的稳定集合。 因此，它通常用来保证给定数量的、完全相同的 Pod 的可用性。

**ReplicaSet 的工作原理**

RepicaSet 是通过一组字段来定义的，包括一个用来识别可获得的 Pod 的集合的选择算符、一个用来标明应该维护的副本个数的数值、一个用来指定应该创建新 Pod 以满足副本个数条件时要使用的 Pod 模板等等。 每个 ReplicaSet 都通过根据需要创建和 删除 Pod 以使得副本个数达到期望值， 进而实现其存在价值。当 ReplicaSet 需要创建新的 Pod 时，会使用所提供的 Pod 模板。

ReplicaSet 通过 Pod 上的 [metadata.ownerReferences](https://kubernetes.io/zh/docs/concepts/workloads/controllers/garbage-collection/#owners-and-dependents) 字段连接到附属 Pod，该字段给出当前对象的属主资源。 ReplicaSet 所获得的 Pod 都在其 ownerReferences 字段中包含了属主 ReplicaSet 的标识信息。正是通过这一连接，ReplicaSet 知道它所维护的 Pod 集合的状态， 并据此计划其操作行为。

ReplicaSet 使用其选择算符来辨识要获得的 Pod 集合。如果某个 Pod 没有 OwnerReference 或者其 OwnerReference 不是一个 [控制器](https://kubernetes.io/zh/docs/concepts/architecture/controller/)，且其匹配到 某 ReplicaSet 的选择算符，则该 Pod 立即被此 ReplicaSet 获得。

**何时使用 ReplicaSet**

ReplicaSet 确保任何时间都有指定数量的 Pod 副本在运行。 然而，Deployment 是一个更高级的概念，它管理 ReplicaSet，并向 Pod 提供声明式的更新以及许多其他有用的功能。 因此，我们建议使用 Deployment 而不是直接使用 ReplicaSet，除非 你需要自定义更新业务流程或根本不需要更新。

这实际上意味着，你可能永远不需要操作 ReplicaSet 对象：而是使用 Deployment，并在 spec 部分定义你的应用。

[`Deployment`](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/) 是一个 可以拥有 ReplicaSet 并使用声明式方式在服务器端完成对 Pods 滚动更新的对象。 尽管 ReplicaSet 可以独立使用，目前它们的主要用途是提供给 Deployment 作为 编排 Pod 创建、删除和更新的一种机制。当使用 Deployment 时，你不必关心 如何管理它所创建的 ReplicaSet，Deployment 拥有并管理其 ReplicaSet。 因此，建议你在需要 ReplicaSet 时使用 Deployment。

**编写 ReplicaSet 的 spec**

与所有其他 Kubernetes API 对象一样，ReplicaSet 也需要 `apiVersion`、`kind`、和 `metadata` 字段。 对于 ReplicaSets 而言，其 kind 始终是 ReplicaSet。 在 Kubernetes 1.9 中，ReplicaSet 上的 API 版本 `apps/v1` 是其当前版本，且被 默认启用。API 版本 `apps/v1beta2` 已被废弃。 参考 `frontend.yaml` 示例的第一行。

ReplicaSet 对象的名称必须是合法的 [DNS 子域名](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/names#dns-subdomain-names)。

ReplicaSet 也需要 [`.spec`](https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status) 部分。

- Pod 模版

`.spec.template` 是一个[Pod 模版](https://kubernetes.io/zh/docs/concepts/workloads/pods/#pod-templates)， 要求设置标签。在 `frontend.yaml` 示例中，我们指定了标签 `tier: frontend`。 注意不要将标签与其他控制器的选择算符重叠，否则那些控制器会尝试收养此 Pod。

对于模板的[重启策略](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy) 字段，`.spec.template.spec.restartPolicy`，唯一允许的取值是 `Always`，这也是默认值.

- Pod 选择算符

`.spec.selector` 字段是一个[标签选择算符](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/labels/)。 如前文中[所讨论的](https://kubernetes.io/zh/docs/concepts/workloads/controllers/replicaset/#how-a-replicaset-works)，这些是用来标识要被获取的 Pods 的标签。在签名的 `frontend.yaml` 示例中，选择算符为：

```yaml
matchLabels:
  tier: frontend
```

在 ReplicaSet 中，`.spec.template.metadata.labels` 的值必须与 `spec.selector` 值 相匹配，否则该配置会被 API 拒绝。

> **说明：**
>
> 对于设置了相同的 `.spec.selector`，但 `.spec.template.metadata.labels` 和 `.spec.template.spec` 字段不同的 两个 ReplicaSet 而言，每个 ReplicaSet 都会忽略被另一个 ReplicaSet 所 创建的 Pods。

- Replicas

你可以通过设置 `.spec.replicas` 来指定要同时运行的 Pod 个数。 ReplicaSet 创建、删除 Pods 以与此值匹配。

如果你没有指定 `.spec.replicas`, 那么默认值为 1。

#### [Deployments](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/)

##### 用例

以下是 Deployments 的典型用例：

- [创建 Deployment 以将 ReplicaSet 上线](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#creating-a-deployment)。 ReplicaSet 在后台创建 Pods。 检查 ReplicaSet 的上线状态，查看其是否成功。
- 通过更新 Deployment 的 PodTemplateSpec，[声明 Pod 的新状态](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#updating-a-deployment) 。 新的 ReplicaSet 会被创建，Deployment 以受控速率将 Pod 从旧 ReplicaSet 迁移到新 ReplicaSet。 每个新的 ReplicaSet 都会更新 Deployment 的修订版本。
- 如果 Deployment 的当前状态不稳定，[回滚到较早的 Deployment 版本](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#rolling-back-a-deployment)。 每次回滚都会更新 Deployment 的修订版本。
- [扩大 Deployment 规模以承担更多负载](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#scaling-a-deployment)。
- [暂停 Deployment](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#pausing-and-resuming-a-deployment) 以应用对 PodTemplateSpec 所作的多项修改， 然后恢复其执行以启动新的上线版本。
- [使用 Deployment 状态](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#deployment-status) 来判定上线过程是否出现停滞。
- [清理较旧的不再需要的 ReplicaSet](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#clean-up-policy) 。

##### 创建 Deployment

下面是 Deployment 示例。其中创建了一个 ReplicaSet，负责启动三个 `nginx` Pods：

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  labels:
    app: nginx
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: nginx:1.14.2
          ports:
            - containerPort: 80
```

在该例中：

- 创建名为 `nginx-deployment`（由 `.metadata.name` 字段标明）的 Deployment。
- 该 Deployment 创建三个（由 `replicas` 字段标明）Pod 副本。

- `selector` 字段定义 Deployment 如何查找要管理的 Pods。 在这里，你只需选择在 Pod 模板中定义的标签（`app: nginx`）。 不过，更复杂的选择规则是也可能的，只要 Pod 模板本身满足所给规则即可。

  > **说明：** `matchLabels` 字段是 `{key,value}` 偶对的映射。在 `matchLabels` 映射中的单个 `{key,value}` 映射等效于 `matchExpressions` 中的一个元素，即其 `key` 字段是 “key”，operator 为 “In”，`value` 数组仅包含 “value”。在 `matchLabels` 和 `matchExpressions` 中给出的所有条件都必须满足才能匹配。

- `template`字段包含以下子字段：
  - Pod 被使用 `labels` 字段打上 `app: nginx` 标签。
  - Pod 模板规约（即 `.template.spec` 字段）指示 Pods 运行一个 `nginx` 容器， 该容器运行版本为 1.14.2 的 `nginx` [Docker Hub](https://hub.docker.com/)镜像。
  - 创建一个容器并使用 `name` 字段将其命名为 `nginx`。

开始之前，请确保的 Kubernetes 集群已启动并运行。 按照以下步骤创建上述 Deployment ：

1. 通过运行以下命令创建 Deployment ：

   ```shell
   kubectl apply -f https://k8s.io/examples/controllers/nginx-deployment.yaml
   ```

   > **说明：** 你可以设置 `--record` 标志将所执行的命令写入资源注解 `kubernetes.io/change-cause` 中。 这对于以后的检查是有用的。例如，要查看针对每个 Deployment 修订版本所执行过的命令。

1. 运行 `kubectl get deployments` 检查 Deployment 是否已创建。如果仍在创建 Deployment， 则输出类似于：

   ```
   NAME               DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
   nginx-deployment   3         0         0            0           1s
   ```

   在检查集群中的 Deployment 时，所显示的字段有：

   - `NAME` 列出了集群中 Deployment 的名称。
   - `READY` 显示应用程序的可用的 _副本_ 数。显示的模式是“就绪个数/期望个数”。
   - `UP-TO-DATE` 显示为了打到期望状态已经更新的副本数。
   - `AVAILABLE` 显示应用可供用户使用的副本数。
   - `AGE` 显示应用程序运行的时间。

   请注意期望副本数是根据 `.spec.replicas` 字段设置 3。

1. 要查看 Deployment 上线状态，运行 `kubectl rollout status deployment.v1.apps/nginx-deployment`。 输出类似于：

   ```
   Waiting for rollout to finish: 2 out of 3 new replicas have been updated...
   deployment "nginx-deployment" successfully rolled out
   ```

1. 几秒钟后再次运行 `kubectl get deployments`。输出类似于：

   ```
   NAME               DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
   nginx-deployment   3         3         3            3           18s
   ```

   注意 Deployment 已创建全部三个副本，并且所有副本都是最新的（它们包含最新的 Pod 模板） 并且可用。

1. 要查看 Deployment 创建的 ReplicaSet（`rs`），运行 `kubectl get rs`。 输出类似于：

   ```
   NAME                          DESIRED   CURRENT   READY   AGE
   nginx-deployment-75675f5897   3         3         3       18s
   ```

   ReplicaSet 输出中包含以下字段：

   - `NAME` 列出名字空间中 ReplicaSet 的名称；
   - `DESIRED` 显示应用的期望副本个数，即在创建 Deployment 时所定义的值。 此为期望状态；
   - `CURRENT` 显示当前运行状态中的副本个数；
   - `READY` 显示应用中有多少副本可以为用户提供服务；
   - `AGE` 显示应用已经运行的时间长度。

   注意 ReplicaSet 的名称始终被格式化为`[Deployment名称]-[随机字符串]`。 其中的随机字符串是使用 pod-template-hash 作为种子随机生成的。

1. 要查看每个 Pod 自动生成的标签，运行 `kubectl get pods --show-labels`。返回以下输出：

   ```
   NAME                                READY     STATUS    RESTARTS   AGE       LABELS
   nginx-deployment-75675f5897-7ci7o   1/1       Running   0          18s       app=nginx,pod-template-hash=3123191453
   nginx-deployment-75675f5897-kzszj   1/1       Running   0          18s       app=nginx,pod-template-hash=3123191453
   nginx-deployment-75675f5897-qqcnn   1/1       Running   0          18s       app=nginx,pod-template-hash=3123191453
   ```

   所创建的 ReplicaSet 确保总是存在三个 `nginx` Pod。

> **说明：** 你必须在 Deployment 中指定适当的选择算符和 Pod 模板标签（在本例中为 `app: nginx`）。 标签或者选择算符不要与其他控制器（包括其他 Deployment 和 StatefulSet）重叠。 Kubernetes 不会阻止你这样做，但是如果多个控制器具有重叠的选择算符，它们可能会发生冲突 执行难以预料的操作。

**Pod-template-hash 标签**

> **说明：** 不要更改此标签。

Deployment 控制器将 `pod-template-hash` 标签添加到 Deployment 所创建或收留的 每个 ReplicaSet 。

此标签可确保 Deployment 的子 ReplicaSets 不重叠。 标签是通过对 ReplicaSet 的 `PodTemplate` 进行哈希处理。 所生成的哈希值被添加到 ReplicaSet 选择算符、Pod 模板标签，并存在于在 ReplicaSet 可能拥有的任何现有 Pod 中。

##### 更新 Deployment

> **说明：** 仅当 Deployment Pod 模板（即 `.spec.template`）发生改变时，例如模板的标签或容器镜像被更新， 才会触发 Deployment 上线。 其他更新（如对 Deployment 执行扩缩容的操作）不会触发上线动作。

按照以下步骤更新 Deployment：

1. 先来更新 nginx Pod 以使用 `nginx:1.16.1` 镜像，而不是 `nginx:1.14.2` 镜像。

   ```shell
   kubectl --record deployment.apps/nginx-deployment set image \
      deployment.v1.apps/nginx-deployment nginx=nginx:1.9.1
   ```

   或者使用下面的命令：

   ```shell
   kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1 --record
   ```

   输出类似于：

   ```
   deployment.apps/nginx-deployment image updated
   ```

   或者，可以 `edit` Deployment 并将 `.spec.template.spec.containers[0].image` 从 `nginx:1.14.2` 更改至 `nginx:1.16.1`。

   ```shell
   kubectl edit deployment.v1.apps/nginx-deployment
   ```

   输出类似于：

   ```
   deployment.apps/nginx-deployment edited
   ```

1. 要查看上线状态，运行：

   ```shell
   kubectl rollout status deployment.v1.apps/nginx-deployment
   ```

   输出类似于：

   ```
   Waiting for rollout to finish: 2 out of 3 new replicas have been updated...
   ```

   或者

   ```
   deployment "nginx-deployment" successfully rolled out
   ```

获取关于已更新的 Deployment 的更多信息：

- 在上线成功后，可以通过运行 `kubectl get deployments` 来查看 Deployment： 输出类似于：

  ```shell
  NAME               DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
  nginx-deployment   3         3         3            3           36s
  ```

- 运行 `kubectl get rs` 以查看 Deployment 通过创建新的 ReplicaSet 并将其扩容到 3 个副本并将旧 ReplicaSet 缩容到 0 个副本完成了 Pod 的更新操作：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```
  NAME                          DESIRED   CURRENT   READY   AGE
  nginx-deployment-1564180365   3         3         3       6s
  nginx-deployment-2035384211   0         0         0       36s
  ```

- 现在运行 `get pods` 应仅显示新的 Pods:

  ```shell
  kubectl get pods
  ```

  输出类似于：

  ```
  NAME                                READY     STATUS    RESTARTS   AGE
  nginx-deployment-1564180365-khku8   1/1       Running   0          14s
  nginx-deployment-1564180365-nacti   1/1       Running   0          14s
  nginx-deployment-1564180365-z9gth   1/1       Running   0          14s
  ```

  下次要更新这些 Pods 时，只需再次更新 Deployment Pod 模板即可。

  Deployment 可确保在更新时仅关闭一定数量的 Pod。默认情况下，它确保至少所需 Pods 75% 处于运行状态（最大不可用比例为 25%）。

  Deployment 还确保仅所创建 Pod 数量只可能比期望 Pods 数高一点点。 默认情况下，它可确保启动的 Pod 个数比期望个数最多多出 25%（最大峰值 25%）。

  例如，如果仔细查看上述 Deployment ，将看到它首先创建了一个新的 Pod，然后删除了一些旧的 Pods， 并创建了新的 Pods。它不会杀死老 Pods，直到有足够的数量新的 Pods 已经出现。 在足够数量的旧 Pods 被杀死前并没有创建新 Pods。它确保至少 2 个 Pod 可用，同时 最多总共 4 个 Pod 可用。

- 获取 Deployment 的更多信息

  ```shell
  kubectl describe deployments
  ```

  输出类似于：

  ```
  Name:                   nginx-deployment
  Namespace:              default
  CreationTimestamp:      Thu, 30 Nov 2017 10:56:25 +0000
  Labels:                 app=nginx
  Annotations:            deployment.kubernetes.io/revision=2
  Selector:               app=nginx
  Replicas:               3 desired | 3 updated | 3 total | 3 available | 0 unavailable
  StrategyType:           RollingUpdate
  MinReadySeconds:        0
  RollingUpdateStrategy:  25% max unavailable, 25% max surge
  Pod Template:
    Labels:  app=nginx
     Containers:
      nginx:
        Image:        nginx:1.16.1
        Port:         80/TCP
        Environment:  <none>
        Mounts:       <none>
      Volumes:        <none>
    Conditions:
      Type           Status  Reason
      ----           ------  ------
      Available      True    MinimumReplicasAvailable
      Progressing    True    NewReplicaSetAvailable
    OldReplicaSets:  <none>
    NewReplicaSet:   nginx-deployment-1564180365 (3/3 replicas created)
    Events:
      Type    Reason             Age   From                   Message
      ----    ------             ----  ----                   -------
      Normal  ScalingReplicaSet  2m    deployment-controller  Scaled up replica set nginx-deployment-2035384211 to 3
      Normal  ScalingReplicaSet  24s   deployment-controller  Scaled up replica set nginx-deployment-1564180365 to 1
      Normal  ScalingReplicaSet  22s   deployment-controller  Scaled down replica set nginx-deployment-2035384211 to 2
      Normal  ScalingReplicaSet  22s   deployment-controller  Scaled up replica set nginx-deployment-1564180365 to 2
      Normal  ScalingReplicaSet  19s   deployment-controller  Scaled down replica set nginx-deployment-2035384211 to 1
      Normal  ScalingReplicaSet  19s   deployment-controller  Scaled up replica set nginx-deployment-1564180365 to 3
      Normal  ScalingReplicaSet  14s   deployment-controller  Scaled down replica set nginx-deployment-2035384211 to 0
  ```

  可以看到，当第一次创建 Deployment 时，它创建了一个 ReplicaSet（nginx-deployment-2035384211） 并将其直接扩容至 3 个副本。更新 Deployment 时，它创建了一个新的 ReplicaSet （nginx-deployment-1564180365），并将其扩容为 1，然后将旧 ReplicaSet 缩容到 2， 以便至少有 2 个 Pod 可用且最多创建 4 个 Pod。 然后，它使用相同的滚动更新策略继续对新的 ReplicaSet 扩容并对旧的 ReplicaSet 缩容。 最后，你将有 3 个可用的副本在新的 ReplicaSet 中，旧 ReplicaSet 将缩容到 0。

**翻转（多 Deployment 动态更新）**

Deployment 控制器每次注意到新的 Deployment 时，都会创建一个 ReplicaSet 以启动所需的 Pods。 如果更新了 Deployment，则控制标签匹配 `.spec.selector` 但模板不匹配 `.spec.template` 的 Pods 的现有 ReplicaSet 被缩容。最终，新的 ReplicaSet 缩放为 `.spec.replicas` 个副本， 所有旧 ReplicaSets 缩放为 0 个副本。

当 Deployment 正在上线时被更新，Deployment 会针对更新创建一个新的 ReplicaSet 并开始对其扩容，之前正在被扩容的 ReplicaSet 会被翻转，添加到旧 ReplicaSets 列表 并开始缩容。

例如，假定你在创建一个 Deployment 以生成 `nginx:1.14.2` 的 5 个副本，但接下来 更新 Deployment 以创建 5 个 `nginx:1.16.1` 的副本，而此时只有 3 个`nginx:1.14.2` 副本已创建。在这种情况下，Deployment 会立即开始杀死 3 个 `nginx:1.14.2` Pods， 并开始创建 `nginx:1.16.1` Pods。它不会等待 `nginx:1.14.2` 的 5 个副本都创建完成 后才开始执行变更动作。

**更改标签选择算符**

通常不鼓励更新标签选择算符。建议你提前规划选择算符。 在任何情况下，如果需要更新标签选择算符，请格外小心，并确保自己了解 这背后可能发生的所有事情。

> **说明：** 在 API 版本 `apps/v1` 中，Deployment 标签选择算符在创建后是不可变的。

- 添加选择算符时要求使用新标签更新 Deployment 规约中的 Pod 模板标签，否则将返回验证错误。 此更改是非重叠的，也就是说新的选择算符不会选择使用旧选择算符所创建的 ReplicaSet 和 Pod， 这会导致创建新的 ReplicaSet 时所有旧 ReplicaSet 都会被孤立。
- 选择算符的更新如果更改了某个算符的键名，这会导致与添加算符时相同的行为。
- 删除选择算符的操作会删除从 Deployment 选择算符中删除现有算符。 此操作不需要更改 Pod 模板标签。现有 ReplicaSet 不会被孤立，也不会因此创建新的 ReplicaSet， 但请注意已删除的标签仍然存在于现有的 Pod 和 ReplicaSet 中。

##### 回滚 Deployment

有时，你可能想要回滚 Deployment；例如，当 Deployment 不稳定时（例如进入反复崩溃状态）。 默认情况下，Deployment 的所有上线记录都保留在系统中，以便可以随时回滚 （你可以通过修改修订历史记录限制来更改这一约束）。

> **说明：** Deployment 被触发上线时，系统就会创建 Deployment 的新的修订版本。 这意味着仅当 Deployment 的 Pod 模板（`.spec.template`）发生更改时，才会创建新修订版本 -- 例如，模板的标签或容器镜像发生变化。 其他更新，如 Deployment 的扩缩容操作不会创建 Deployment 修订版本。 这是为了方便同时执行手动缩放或自动缩放。 换言之，当你回滚到较早的修订版本时，只有 Deployment 的 Pod 模板部分会被回滚。

- 假设你在更新 Deployment 时犯了一个拼写错误，将镜像名称命名设置为 `nginx:1.161` 而不是 `nginx:1.16.1`：

  ```shell
  kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.161 --record=true
  ```

  输出类似于：

  ```shell
  deployment.apps/nginx-deployment image updated
  ```

- 此上线进程会出现停滞。你可以通过检查上线状态来验证：

  ```shell
  kubectl rollout status deployment.v1.apps/nginx-deployment
  ```

  输出类似于：

  ```
  Waiting for rollout to finish: 1 out of 3 new replicas have been updated...
  ```

- 按 Ctrl-C 停止上述上线状态观测。有关上线停滞的详细信息，[参考这里](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#deployment-status)。

- 你可以看到旧的副本有两个（`nginx-deployment-1564180365` 和 `nginx-deployment-2035384211`）， 新的副本有 1 个（`nginx-deployment-3066724191`）：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```shell
  NAME                          DESIRED   CURRENT   READY   AGE
  nginx-deployment-1564180365   3         3         3       25s
  nginx-deployment-2035384211   0         0         0       36s
  nginx-deployment-3066724191   1         1         0       6s
  ```

- 查看所创建的 Pod，你会注意到新 ReplicaSet 所创建的 1 个 Pod 卡顿在镜像拉取循环中。

  ```shell
  kubectl get pods
  ```

  输出类似于：

  ```shell
  NAME                                READY     STATUS             RESTARTS   AGE
  nginx-deployment-1564180365-70iae   1/1       Running            0          25s
  nginx-deployment-1564180365-jbqqo   1/1       Running            0          25s
  nginx-deployment-1564180365-hysrc   1/1       Running            0          25s
  nginx-deployment-3066724191-08mng   0/1       ImagePullBackOff   0          6s
  ```

  > **说明：** Deployment 控制器自动停止有问题的上线过程，并停止对新的 ReplicaSet 扩容。 这行为取决于所指定的 rollingUpdate 参数（具体为 `maxUnavailable`）。 默认情况下，Kubernetes 将此值设置为 25%。

- 获取 Deployment 描述信息：

  ```shell
  kubectl describe deployment
  ```

  输出类似于：

  ```shell
  Name:           nginx-deployment
  Namespace:      default
  CreationTimestamp:  Tue, 15 Mar 2016 14:48:04 -0700
  Labels:         app=nginx
  Selector:       app=nginx
  Replicas:       3 desired | 1 updated | 4 total | 3 available | 1 unavailable
  StrategyType:       RollingUpdate
  MinReadySeconds:    0
  RollingUpdateStrategy:  25% max unavailable, 25% max surge
  Pod Template:
    Labels:  app=nginx
    Containers:
     nginx:
      Image:        nginx:1.91
      Port:         80/TCP
      Host Port:    0/TCP
      Environment:  <none>
      Mounts:       <none>
    Volumes:        <none>
  Conditions:
    Type           Status  Reason
    ----           ------  ------
    Available      True    MinimumReplicasAvailable
    Progressing    True    ReplicaSetUpdated
  OldReplicaSets:     nginx-deployment-1564180365 (3/3 replicas created)
  NewReplicaSet:      nginx-deployment-3066724191 (1/1 replicas created)
  Events:
    FirstSeen LastSeen    Count   From                    SubobjectPath   Type        Reason              Message
    --------- --------    -----   ----                    -------------   --------    ------              -------
    1m        1m          1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled up replica set nginx-deployment-2035384211 to 3
    22s       22s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled up replica set nginx-deployment-1564180365 to 1
    22s       22s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled down replica set nginx-deployment-2035384211 to 2
    22s       22s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled up replica set nginx-deployment-1564180365 to 2
    21s       21s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled down replica set nginx-deployment-2035384211 to 1
    21s       21s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled up replica set nginx-deployment-1564180365 to 3
    13s       13s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled down replica set nginx-deployment-2035384211 to 0
    13s       13s         1       {deployment-controller }                Normal      ScalingReplicaSet   Scaled up replica set nginx-deployment-3066724191 to 1
  ```

  要解决此问题，需要回滚到以前稳定的 Deployment 版本。

**检查 Deployment 上线历史**

按照如下步骤检查回滚历史：

1. 首先，检查 Deployment 修订历史：

   ```shell
   kubectl rollout history deployment.v1.apps/nginx-deployment
   ```

   输出类似于：

   ```shell
   deployments "nginx-deployment"
   REVISION    CHANGE-CAUSE
   1           kubectl apply --filename=https://k8s.io/examples/controllers/nginx-deployment.yaml --record=true
   2           kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.9.1 --record=true
   3           kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.91 --record=true
   ```

   `CHANGE-CAUSE` 的内容是从 Deployment 的 `kubernetes.io/change-cause` 注解复制过来的。 复制动作发生在修订版本创建时。你可以通过以下方式设置 `CHANGE-CAUSE` 消息：

   - 使用 `kubectl annotate deployment.v1.apps/nginx-deployment kubernetes.io/change-cause="image updated to 1.9.1"` 为 Deployment 添加注解。
   - 追加 `--record` 命令行标志以保存正在更改资源的 `kubectl` 命令。
   - 手动编辑资源的清单。

1. 要查看修订历史的详细信息，运行：

   ```shell
   kubectl rollout history deployment.v1.apps/nginx-deployment --revision=2
   ```

   输出类似于：

   ```shell
   deployments "nginx-deployment" revision 2
     Labels:       app=nginx
             pod-template-hash=1159050644
     Annotations:  kubernetes.io/change-cause=kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.16.1 --record=true
     Containers:
      nginx:
       Image:      nginx:1.16.1
       Port:       80/TCP
        QoS Tier:
           cpu:      BestEffort
           memory:   BestEffort
       Environment Variables:      <none>
     No volumes.
   ```

**回滚到之前的修订版本**

按照下面给出的步骤将 Deployment 从当前版本回滚到以前的版本（即版本 2）。

1. 假定现在你已决定撤消当前上线并回滚到以前的修订版本：

   ```shell
   kubectl rollout undo deployment.v1.apps/nginx-deployment
   ```

   输出类似于：

   ```
   deployment.apps/nginx-deployment
   ```

   或者，你也可以通过使用 `--to-revision` 来回滚到特定修订版本：

   ```shell
   kubectl rollout undo deployment.v1.apps/nginx-deployment --to-revision=2
   ```

   输出类似于：

   ```
   deployment.apps/nginx-deployment
   ```

   与回滚相关的指令的更详细信息，请参考 [`kubectl rollout`](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#rollout)。

   现在，Deployment 正在回滚到以前的稳定版本。正如你所看到的，Deployment 控制器生成了 回滚到修订版本 2 的 `DeploymentRollback` 事件。

1. 检查回滚是否成功以及 Deployment 是否正在运行，运行：

   ```shell
   kubectl get deployment nginx-deployment
   ```

   输出类似于：

   ```shell
   NAME               DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
   nginx-deployment   3         3         3            3           30m
   ```

1. 获取 Deployment 描述信息：

   ```shell
   kubectl describe deployment nginx-deployment
   ```

   输出类似于：

   ```
   Name:                   nginx-deployment
   Namespace:              default
   CreationTimestamp:      Sun, 02 Sep 2018 18:17:55 -0500
   Labels:                 app=nginx
   Annotations:            deployment.kubernetes.io/revision=4
                           kubernetes.io/change-cause=kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.16.1 --record=true
   Selector:               app=nginx
   Replicas:               3 desired | 3 updated | 3 total | 3 available | 0 unavailable
   StrategyType:           RollingUpdate
   MinReadySeconds:        0
   RollingUpdateStrategy:  25% max unavailable, 25% max surge
   Pod Template:
     Labels:  app=nginx
     Containers:
      nginx:
       Image:        nginx:1.16.1
       Port:         80/TCP
       Host Port:    0/TCP
       Environment:  <none>
       Mounts:       <none>
     Volumes:        <none>
   Conditions:
     Type           Status  Reason
     ----           ------  ------
     Available      True    MinimumReplicasAvailable
     Progressing    True    NewReplicaSetAvailable
   OldReplicaSets:  <none>
   NewReplicaSet:   nginx-deployment-c4747d96c (3/3 replicas created)
   Events:
     Type    Reason              Age   From                   Message
     ----    ------              ----  ----                   -------
     Normal  ScalingReplicaSet   12m   deployment-controller  Scaled up replica set nginx-deployment-75675f5897 to 3
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled up replica set nginx-deployment-c4747d96c to 1
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled down replica set nginx-deployment-75675f5897 to 2
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled up replica set nginx-deployment-c4747d96c to 2
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled down replica set nginx-deployment-75675f5897 to 1
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled up replica set nginx-deployment-c4747d96c to 3
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled down replica set nginx-deployment-75675f5897 to 0
     Normal  ScalingReplicaSet   11m   deployment-controller  Scaled up replica set nginx-deployment-595696685f to 1
     Normal  DeploymentRollback  15s   deployment-controller  Rolled back deployment "nginx-deployment" to revision 2
     Normal  ScalingReplicaSet   15s   deployment-controller  Scaled down replica set nginx-deployment-595696685f to 0
   ```

##### 缩放 Deployment

你可以使用如下指令缩放 Deployment：

```shell
kubectl scale deployment.v1.apps/nginx-deployment --replicas=10
```

输出类似于：

```
deployment.apps/nginx-deployment scaled
```

假设集群启用了[Pod 的水平自动缩放](https://kubernetes.io/zh/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/)， 你可以为 Deployment 设置自动缩放器，并基于现有 Pods 的 CPU 利用率选择 要运行的 Pods 个数下限和上限。

```shell
kubectl autoscale deployment.v1.apps/nginx-deployment --min=10 --max=15 --cpu-percent=80
```

输出类似于：

```
deployment.apps/nginx-deployment scaled
```

**比例缩放**

RollingUpdate 的 Deployment 支持同时运行应用程序的多个版本。 当自动缩放器缩放处于上线进程（仍在进行中或暂停）中的 RollingUpdate Deployment 时， Deployment 控制器会平衡现有的活跃状态的 ReplicaSets（含 Pods 的 ReplicaSets）中的额外副本， 以降低风险。这称为 _比例缩放（Proportional Scaling）_。

例如，你正在运行一个 10 个副本的 Deployment，其 [maxSurge](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#max-surge)=3，[maxUnavailable](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#max-unavailable)=2。

- 确保 Deployment 的这 10 个副本都在运行。

  ```shell
  kubectl get deploy
  ```

  输出类似于：

  ```
  NAME                 DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
  nginx-deployment     10        10        10           10          50s
  ```

- 更新 Deployment 使用新镜像，碰巧该镜像无法从集群内部解析。

  ```shell
  kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:sometag
  ```

  输出类似于：

  ```
  deployment.apps/nginx-deployment image updated
  ```

- 镜像更新使用 ReplicaSet `nginx-deployment-1989198191` 启动新的上线过程， 但由于上面提到的 `maxUnavailable` 要求，该进程被阻塞了。检查上线状态：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```
  NAME                          DESIRED   CURRENT   READY     AGE
  nginx-deployment-1989198191   5         5         0         9s
  nginx-deployment-618515232    8         8         8         1m
  ```

- 然后，出现了新的 Deployment 扩缩请求。自动缩放器将 Deployment 副本增加到 15。 Deployment 控制器需要决定在何处添加 5 个新副本。如果未使用比例缩放，所有 5 个副本 都将添加到新的 ReplicaSet 中。使用比例缩放时，可以将额外的副本分布到所有 ReplicaSet。 较大比例的副本会被添加到拥有最多副本的 ReplicaSet，而较低比例的副本会进入到 副本较少的 ReplicaSet。所有剩下的副本都会添加到副本最多的 ReplicaSet。 具有零副本的 ReplicaSets 不会被扩容。

在上面的示例中，3 个副本被添加到旧 ReplicaSet 中，2 个副本被添加到新 ReplicaSet。 假定新的副本都很健康，上线过程最终应将所有副本迁移到新的 ReplicaSet 中。 要确认这一点，请运行：

```shell
kubectl get deploy
```

输出类似于：

```
NAME                 DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
nginx-deployment     15        18        7            8           7m
```

上线状态确认了副本是如何被添加到每个 ReplicaSet 的。

```shell
kubectl get rs
```

输出类似于：

```shell
NAME                          DESIRED   CURRENT   READY     AGE
nginx-deployment-1989198191   7         7         0         7m
nginx-deployment-618515232    11        11        11        7m
```

##### 暂停、恢复 Deployment

你可以在触发一个或多个更新之前暂停 Deployment，然后再恢复其执行。 这样做使得你能够在暂停和恢复执行之间应用多个修补程序，而不会触发不必要的上线操作。

- 例如，对于一个刚刚创建的 Deployment： 获取 Deployment 信息：

  ```shell
  kubectl get deploy
  ```

  输出类似于：

  ```
  NAME      DESIRED   CURRENT   UP-TO-DATE   AVAILABLE   AGE
  nginx     3         3         3            3           1m
  ```

  获取上线状态：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```shell
  NAME               DESIRED   CURRENT   READY     AGE
  nginx-2142116321   3         3         3         1m
  ```

- 使用如下指令暂停运行：

  ```shell
  kubectl rollout pause deployment.v1.apps/nginx-deployment
  ```

  输出类似于：

  ```shell
  deployment.apps/nginx-deployment paused
  ```

- 接下来更新 Deployment 镜像：

  ```shell
  kubectl set image deployment.v1.apps/nginx-deployment nginx=nginx:1.16.1
  ```

  输出类似于：

  ```
  deployment.apps/nginx-deployment image updated
  ```

- 注意没有新的上线被触发：

  ```shell
  kubectl rollout history deployment.v1.apps/nginx-deployment
  ```

  输出类似于：

  ```shell
  deployments "nginx"
  REVISION  CHANGE-CAUSE
  1   <none>
  ```

- 获取上线状态确保 Deployment 更新已经成功：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```shell
  NAME               DESIRED   CURRENT   READY     AGE
  nginx-2142116321   3         3         3         2m
  ```

- 你可以根据需要执行很多更新操作，例如，可以要使用的资源：

  ```shell
  kubectl set resources deployment.v1.apps/nginx-deployment -c=nginx --limits=cpu=200m,memory=512Mi
  ```

  输出类似于：

  ```
  deployment.apps/nginx-deployment resource requirements updated
  ```

  暂停 Deployment 之前的初始状态将继续发挥作用，但新的更新在 Deployment 被 暂停期间不会产生任何效果。

- 最终，恢复 Deployment 执行并观察新的 ReplicaSet 的创建过程，其中包含了所应用的所有更新：

  ```shell
  kubectl rollout resume deployment.v1.apps/nginx-deployment
  ```

  输出：

  ```shell
  deployment.apps/nginx-deployment resumed
  ```

- 观察上线的状态，直到完成。

  ```shell
  kubectl get rs -w
  ```

  输出类似于：

  ```
  NAME               DESIRED   CURRENT   READY     AGE
  nginx-2142116321   2         2         2         2m
  nginx-3926361531   2         2         0         6s
  nginx-3926361531   2         2         1         18s
  nginx-2142116321   1         2         2         2m
  nginx-2142116321   1         2         2         2m
  nginx-3926361531   3         2         1         18s
  nginx-3926361531   3         2         1         18s
  nginx-2142116321   1         1         1         2m
  nginx-3926361531   3         3         1         18s
  nginx-3926361531   3         3         2         19s
  nginx-2142116321   0         1         1         2m
  nginx-2142116321   0         1         1         2m
  nginx-2142116321   0         0         0         2m
  nginx-3926361531   3         3         3         20s
  ```

- 获取最近上线的状态：

  ```shell
  kubectl get rs
  ```

  输出类似于：

  ```
  NAME               DESIRED   CURRENT   READY     AGE
  nginx-2142116321   0         0         0         2m
  nginx-3926361531   3         3         3         28s
  ```

> **说明：** 你不可以回滚处于暂停状态的 Deployment，除非先恢复其执行状态。

##### Deployment 状态

Deployment 的生命周期中会有许多状态。上线新的 ReplicaSet 期间可能处于 [Progressing（进行中）](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#progressing-deployment)，可能是 [Complete（已完成）](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#complete-deployment)，也可能是 [Failed（失败）](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#failed-deployment)以至于无法继续进行。

**进行中的 Deployment**

执行下面的任务期间，Kubernetes 标记 Deployment 为 _进行中（Progressing）_：

- Deployment 创建新的 ReplicaSet
- Deployment 正在为其最新的 ReplicaSet 扩容
- Deployment 正在为其旧有的 ReplicaSet(s) 缩容
- 新的 Pods 已经就绪或者可用（就绪至少持续了 [MinReadySeconds](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#min-ready-seconds) 秒）。

你可以使用 `kubectl rollout status` 监视 Deployment 的进度。

**完成的 Deployment**

当 Deployment 具有以下特征时，Kubernetes 将其标记为 _完成（Complete）_：

- 与 Deployment 关联的所有副本都已更新到指定的最新版本，这意味着之前请求的所有更新都已完成。
- 与 Deployment 关联的所有副本都可用。
- 未运行 Deployment 的旧副本。

你可以使用 `kubectl rollout status` 检查 Deployment 是否已完成。 如果上线成功完成，`kubectl rollout status` 返回退出代码 0。

```shell
kubectl rollout status deployment.v1.apps/nginx-deployment
```

输出类似于：

```shell
Waiting for rollout to finish: 2 of 3 updated replicas are available...
deployment "nginx-deployment" successfully rolled out
$ echo $?
0
```

**失败的 Deployment**

你的 Deployment 可能会在尝试部署其最新的 ReplicaSet 受挫，一直处于未完成状态。 造成此情况一些可能因素如下：

- 配额（Quota）不足
- 就绪探测（Readiness Probe）失败
- 镜像拉取错误
- 权限不足
- 限制范围（Limit Ranges）问题
- 应用程序运行时的配置错误

检测此状况的一种方法是在 Deployment 规约中指定截止时间参数： （[`.spec.progressDeadlineSeconds`]（#progress-deadline-seconds））。 `.spec.progressDeadlineSeconds` 给出的是一个秒数值，Deployment 控制器在（通过 Deployment 状态） 标示 Deployment 进展停滞之前，需要等待所给的时长。

以下 `kubectl` 命令设置规约中的 `progressDeadlineSeconds`，从而告知控制器 在 10 分钟后报告 Deployment 没有进展：

```shell
kubectl patch deployment.v1.apps/nginx-deployment -p '{"spec":{"progressDeadlineSeconds":600}}'
```

输出类似于：

```
deployment.apps/nginx-deployment patched
```

超过截止时间后，Deployment 控制器将添加具有以下属性的 DeploymentCondition 到 Deployment 的 `.status.conditions` 中：

- Type=Progressing
- Status=False
- Reason=ProgressDeadlineExceeded

参考 [Kubernetes API 约定](https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#typical-status-properties) 获取更多状态状况相关的信息。

> **说明：**
>
> 除了报告 `Reason=ProgressDeadlineExceeded` 状态之外，Kubernetes 对已停止的 Deployment 不执行任何操作。更高级别的编排器可以利用这一设计并相应地采取行动。 例如，将 Deployment 回滚到其以前的版本。
>
> 如果你暂停了某个 Deployment，Kubernetes 不再根据指定的截止时间检查 Deployment 进展。 你可以在上线过程中间安全地暂停 Deployment 再恢复其执行，这样做不会导致超出最后时限的问题。

Deployment 可能会出现瞬时性的错误，可能因为设置的超时时间过短， 也可能因为其他可认为是临时性的问题。例如，假定所遇到的问题是配额不足。 如果描述 Deployment，你将会注意到以下部分：

```shell
kubectl describe deployment nginx-deployment
```

输出类似于：

```
<...>
Conditions:
  Type            Status  Reason
  ----            ------  ------
  Available       True    MinimumReplicasAvailable
  Progressing     True    ReplicaSetUpdated
  ReplicaFailure  True    FailedCreate
<...>
```

如果运行 `kubectl get deployment nginx-deployment -o yaml`，Deployment 状态输出 将类似于这样：

```
status:
  availableReplicas: 2
  conditions:
  - lastTransitionTime: 2016-10-04T12:25:39Z
    lastUpdateTime: 2016-10-04T12:25:39Z
    message: Replica set "nginx-deployment-4262182780" is progressing.
    reason: ReplicaSetUpdated
    status: "True"
    type: Progressing
  - lastTransitionTime: 2016-10-04T12:25:42Z
    lastUpdateTime: 2016-10-04T12:25:42Z
    message: Deployment has minimum availability.
    reason: MinimumReplicasAvailable
    status: "True"
    type: Available
  - lastTransitionTime: 2016-10-04T12:25:39Z
    lastUpdateTime: 2016-10-04T12:25:39Z
    message: 'Error creating: pods "nginx-deployment-4262182780-" is forbidden: exceeded quota:
      object-counts, requested: pods=1, used: pods=3, limited: pods=2'
    reason: FailedCreate
    status: "True"
    type: ReplicaFailure
  observedGeneration: 3
  replicas: 2
  unavailableReplicas: 2
```

最终，一旦超过 Deployment 进度限期，Kubernetes 将更新状态和进度状况的原因：

```
Conditions:
  Type            Status  Reason
  ----            ------  ------
  Available       True    MinimumReplicasAvailable
  Progressing     False   ProgressDeadlineExceeded
  ReplicaFailure  True    FailedCreate
```

可以通过缩容 Deployment 或者缩容其他运行状态的控制器，或者直接在命名空间中增加配额 来解决配额不足的问题。如果配额条件满足，Deployment 控制器完成了 Deployment 上线操作， Deployment 状态会更新为成功状况（`Status=True` and `Reason=NewReplicaSetAvailable`）。

```
Conditions:
  Type          Status  Reason
  ----          ------  ------
  Available     True    MinimumReplicasAvailable
  Progressing   True    NewReplicaSetAvailable
```

`Type=Available` 加上 `Status=True` 意味着 Deployment 具有最低可用性。 最低可用性由 Deployment 策略中的参数指定。 `Type=Progressing` 加上 `Status=True` 表示 Deployment 处于上线过程中，并且正在运行， 或者已成功完成进度，最小所需新副本处于可用。 请参阅对应状况的 Reason 了解相关细节。 在我们的案例中 `Reason=NewReplicaSetAvailable` 表示 Deployment 已完成。

你可以使用 `kubectl rollout status` 检查 Deployment 是否未能取得进展。 如果 Deployment 已超过进度限期，`kubectl rollout status` 返回非零退出代码。

```shell
kubectl rollout status deployment.v1.apps/nginx-deployment
```

输出类似于：

```
Waiting for rollout to finish: 2 out of 3 new replicas have been updated...
error: deployment "nginx" exceeded its progress deadline
$ echo $?
1
```

**对失败 Deployment 的操作**

可应用于已完成的 Deployment 的所有操作也适用于失败的 Deployment。 你可以对其执行扩缩容、回滚到以前的修订版本等操作，或者在需要对 Deployment 的 Pod 模板应用多项调整时，将 Deployment 暂停。

##### 清理策略

你可以在 Deployment 中设置 `.spec.revisionHistoryLimit` 字段以指定保留此 Deployment 的多少个旧有 ReplicaSet。其余的 ReplicaSet 将在后台被垃圾回收。 默认情况下，此值为 10。

> **说明：** 显式将此字段设置为 0 将导致 Deployment 的所有历史记录被清空，因此 Deployment 将无法回滚。

##### 金丝雀部署

如果要使用 Deployment 向用户子集或服务器子集上线版本，则可以遵循 [资源管理](https://kubernetes.io/zh/docs/concepts/cluster-administration/manage-deployment/#canary-deployments) 所描述的金丝雀模式，创建多个 Deployment，每个版本一个。

##### 编写 Deployment 规约

同其他 Kubernetes 配置一样， Deployment 需要 `apiVersion`，`kind` 和 `metadata` 字段。 有关配置文件的其他信息，请参考 [部署 Deployment ](https://kubernetes.io/zh/docs/tasks/run-application/run-stateless-application-deployment/)、配置容器和 [使用 kubectl 管理资源](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/object-management/)等相关文档。

Deployment 对象的名称必须是合法的 [DNS 子域名](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/names#dns-subdomain-names)。 Deployment 还需要 [`.spec` 部分](https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#spec-and-status)。

**Pod 模板**

`.spec` 中只有 `.spec.template` 和 `.spec.selector` 是必需的字段。

`.spec.template` 是一个 [Pod 模板](https://kubernetes.io/zh/docs/concepts/workloads/pods/#pod-templates)。 它和 [Pod](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/) 的语法规则完全相同。 只是这里它是嵌套的，因此不需要 `apiVersion` 或 `kind`。

除了 Pod 的必填字段外，Deployment 中的 Pod 模板必须指定适当的标签和适当的重新启动策略。 对于标签，请确保不要与其他控制器重叠。请参考[选择算符](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#selector)。

只有 [`.spec.template.spec.restartPolicy`](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy) 等于 `Always` 才是被允许的，这也是在没有指定时的默认设置。

**副本**

`.spec.replicas` 是指定所需 Pod 的可选字段。它的默认值是 1。

**选择算符**

`.spec.selector` 是指定本 Deployment 的 Pod [标签选择算符](https://kubernetes.io/zh/docs/concepts/overview/working-with-objects/labels/)的必需字段。

`.spec.selector` 必须匹配 `.spec.template.metadata.labels`，否则请求会被 API 拒绝。

在 API `apps/v1`版本中，`.spec.selector` 和 `.metadata.labels` 如果没有设置的话， 不会被默认设置为 `.spec.template.metadata.labels`，所以需要明确进行设置。 同时在 `apps/v1`版本中，Deployment 创建后 `.spec.selector` 是不可变的。

当 Pod 的标签和选择算符匹配，但其模板和 `.spec.template` 不同时，或者此类 Pod 的总数超过 `.spec.replicas` 的设置时，Deployment 会终结之。 如果 Pods 总数未达到期望值，Deployment 会基于 `.spec.template` 创建新的 Pod。

> **说明：** 你不应直接创建、或者通过创建另一个 Deployment，或者创建类似 ReplicaSet 或 ReplicationController 这类控制器来创建标签与此选择算符匹配的 Pod。 如果这样做，第一个 Deployment 会认为它创建了这些 Pod。 Kubernetes 不会阻止你这么做。

如果有多个控制器的选择算符发生重叠，则控制器之间会因冲突而无法正常工作。

**策略**

`.spec.strategy` 策略指定用于用新 Pods 替换旧 Pods 的策略。 `.spec.strategy.type` 可以是 “Recreate” 或 “RollingUpdate”。“RollingUpdate” 是默认值。

**重新创建 Deployment**

如果 `.spec.strategy.type==Recreate`，在创建新 Pods 之前，所有现有的 Pods 会被杀死。

**滚动更新 Deployment**

Deployment 会在 `.spec.strategy.type==RollingUpdate`时，采取 滚动更新的方式更新 Pods。你可以指定 `maxUnavailable` 和 `maxSurge` 来控制滚动更新 过程。

**最大不可用**

`.spec.strategy.rollingUpdate.maxUnavailable` 是一个可选字段，用来指定 更新过程中不可用的 Pod 的个数上限。该值可以是绝对数字（例如，5），也可以是 所需 Pods 的百分比（例如，10%）。百分比值会转换成绝对数并去除小数部分。 如果 `.spec.strategy.rollingUpdate.maxSurge` 为 0，则此值不能为 0。 默认值为 25%。

例如，当此值设置为 30% 时，滚动更新开始时会立即将旧 ReplicaSet 缩容到期望 Pod 个数的 70%。 新 Pod 准备就绪后，可以继续缩容旧有的 ReplicaSet，然后对新的 ReplicaSet 扩容，确保在更新期间 可用的 Pods 总数在任何时候都至少为所需的 Pod 个数的 70%。

**最大峰值**

`.spec.strategy.rollingUpdate.maxSurge` 是一个可选字段，用来指定可以创建的超出 期望 Pod 个数的 Pod 数量。此值可以是绝对数（例如，5）或所需 Pods 的百分比（例如，10%）。 如果 `MaxUnavailable` 为 0，则此值不能为 0。百分比值会通过向上取整转换为绝对数。 此字段的默认值为 25%。

例如，当此值为 30% 时，启动滚动更新后，会立即对新的 ReplicaSet 扩容，同时保证新旧 Pod 的总数不超过所需 Pod 总数的 130%。一旦旧 Pods 被杀死，新的 ReplicaSet 可以进一步扩容， 同时确保更新期间的任何时候运行中的 Pods 总数最多为所需 Pods 总数的 130%。

**进度期限秒数**

`.spec.progressDeadlineSeconds` 是一个可选字段，用于指定系统在报告 Deployment [进展失败](https://kubernetes.io/zh/docs/concepts/workloads/controllers/deployment/#failed-deployment) 之前等待 Deployment 取得进展的秒数。 这类报告会在资源状态中体现为 `Type=Progressing`、`Status=False`、 `Reason=ProgressDeadlineExceeded`。Deployment 控制器将持续重试 Deployment。 将来，一旦实现了自动回滚，Deployment 控制器将在探测到这样的条件时立即回滚 Deployment。

如果指定，则此字段值需要大于 `.spec.minReadySeconds` 取值。

**最短就绪时间**

`.spec.minReadySeconds` 是一个可选字段，用于指定新创建的 Pod 在没有任意容器崩溃情况下的最小就绪时间， 只有超出这个时间 Pod 才被视为可用。默认值为 0（Pod 在准备就绪后立即将被视为可用）。 要了解何时 Pod 被视为就绪，可参考[容器探针](https://kubernetes.io/zh/docs/concepts/workloads/pods/pod-lifecycle/#container-probes)。

**修订历史限制**

Deployment 的修订历史记录存储在它所控制的 ReplicaSets 中。

`.spec.revisionHistoryLimit` 是一个可选字段，用来设定出于会滚目的所要保留的旧 ReplicaSet 数量。 这些旧 ReplicaSet 会消耗 etcd 中的资源，并占用 `kubectl get rs` 的输出。 每个 Deployment 修订版本的配置都存储在其 ReplicaSets 中；因此，一旦删除了旧的 ReplicaSet， 将失去回滚到 Deployment 的对应修订版本的能力。 默认情况下，系统保留 10 个旧 ReplicaSet，但其理想值取决于新 Deployment 的频率和稳定性。

更具体地说，将此字段设置为 0 意味着将清理所有具有 0 个副本的旧 ReplicaSet。 在这种情况下，无法撤消新的 Deployment 上线，因为它的修订历史被清除了。

**paused（暂停的）**

`.spec.paused` 是用于暂停和恢复 Deployment 的可选布尔字段。 暂停的 Deployment 和未暂停的 Deployment 的唯一区别是，Deployment 处于暂停状态时， PodTemplateSpec 的任何修改都不会触发新的上线。 Deployment 在创建时是默认不会处于暂停状态。

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
