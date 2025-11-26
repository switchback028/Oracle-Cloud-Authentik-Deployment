# Oracle-Cloud-Authentik-Deployment

## Forward
I've always had a facination with cloud providers (AWS, GCP, Azure) but my day job really never gave me the opportunity to try out the features and capabilities that these public cloud providers have. Plus, these cloud providers often have a 30 day trial window after which it gets extremely expensive and frankly is a bit cost prohibitive for my tastes. However, I have found the Oracle Cloud free tier to be pretty impressive and generous in its free-tier-ness. So, after spinning up an account I decided to give myself a goal. Right now my Colo-lab datacenter instances are using a legacy LDAP provider to provide SSO for my public services (Nextcloud, Mail, Gitlab, etc). I've been wanting to try Authentik out but couldn't really settle on a reasonable highly-available configuration that didn't require me to re-architect both my east coast and west coast server cabinets. I want to demo putting Authentik in a public cloud environment behind a load balancer and have it serve SAML/OIDC to my self-hosted services. I already have a failover plan for those systems, but tying it all together with a cloud-native SSO is the icing on the cake.

## Goals
- Integrate Ansible playbooks to make changes and configure systems inside Oracle's Cloud Infrastructure.
- Deploy a Load Balancer at Free Tier
- Deploy Two or Three Ampere instances using Ubuntu or Rocky Linux
- Deploy HA-ready Authentik with Postgres DB replication on each instance (The Oracle Cloud free DB doesn't have enough capabilities to leverage their managed DB infrastructure sadly) 
