# 跨地域、VPC、账号部署场景常见问题 {#concept_hr4_xsl_xdb .concept}

数据库审计系统支持跨地域、跨VPC、跨账号服务器的数据库审计。只需要RDS或ECS实例与数据库审计系统之间网络互通，即可将不同地域、不同VPC网络、不同账号中的服务器接入数据库审计系统进行审计。

例如，您在一个阿里云账号下有10多台服务器，分别在华北1、2、3三个不同地域。只要这些服务器与数据库审计系统网络互通，您就可以使用一个数据库审计实例对这些服务器中的数据库进行审计。

例如，您在一个阿里云账号下有13台ECS，其中9台使用经典网络，4台使用VPC专有网络。只要经典网络和VPC中的服务器与数据库审计系统网络互通，您就可以使用一个数据库审计实例对这些服务器中的数据库进行审计。

**说明：** 如果服务器与数据库审计系统之间网络无法连通，则您可能需要多台数据库审计实例接入不同的服务器进行数据库审计。

