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
