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

#### Init 容器

#### Pod 拓扑分布约束

#### 干扰（Disruptions）

#### 临时容器

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
