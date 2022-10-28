# pol-driven-gov-demo

## Custom policies
- see /exportedpolicies/
Includes:
- Automated AD domain join
- Automating enabling VMs for host-based encryption, which - alongside SSE on disks - provides the equivalent of ADE/bitlocker/dmcrypt etc for encryption at rest, encrytion in place (hypervisor process/memory), and in transit (between running VM and disk) without performance overhead.
- Enabling VM OS and other managed disks for Server Side Encyption (ading to existing Disk Encryption Set)

## Policy assignments:
Note: in addition to assignments for the custom policies listed above, these built-in policies are assigned to the scope where VMs are deployed/running:
- Deploy pre-reqs for Guest Configuration:
  - https://portal.azure.com/#view/Microsoft_Azure_Policy/InitiativeDetailBlade/id/%2Fproviders%2FMicrosoft.Authorization%2FpolicySetDefinitions%2F12794019-7a00-42cf-95c2-882eed337cc8/scopes~/%5B%22%2Fsubscriptions%2F8f27126c-bea5-4d4e-bc71-4b571ddf9684%22%5D
- Private Endpoints for Guest COnfiguration assignments should be enabled:
  - https://portal.azure.com/#view/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F480d0f91-30af-4a76-9afb-f5710ac52b09
- Audit Windows machines that are not joined to the specified Domain:
  - https://portal.azure.com/#view/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F84662df4-0e37-44a6-9ce1-c9d2150db18c
- [Preview]: Windows machines should meet requirements for the Azure compute security baseline
  - https://portal.azure.com/#view/Microsoft_Azure_Policy/InitiativeDetailBlade/id/%2Fproviders%2FMicrosoft.Authorization%2FpolicySetDefinitions%2Fbe7a78aa-3e10-4153-a5fd-8c6506dbc821/scopes~/%5B%22%2Fsubscriptions%2F8f27126c-bea5-4d4e-bc71-4b571ddf9684%22%5D

