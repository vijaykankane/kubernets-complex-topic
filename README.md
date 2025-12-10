# kubernets-complex-topic
kubernets-complex-topic

1. LimitRange usage and its explaination

1️⃣ defaultRequest

This is the resource request automatically applied when a user does not specify resources.requests.

It affects scheduling.

Kubernetes uses requests to decide which node a Pod can fit on.

2️⃣ default

This is the resource limit automatically applied when a user does not specify resources.limits.

Limits affect maximum allowed usage of a container.
defaultRequest = what pod asks for (scheduling baseline)

default = maximum it can use (runtime cap)
   

3. Use of the resource Qouta at the namespace level so we can isolate the usage among multiple namespace users among shared cluster
   



| Feature                                            | LimitRange | ResourceQuota |
| -------------------------------------------------- | ---------- | ------------- |
| Controls per Pod/Container size                    | ✅ Yes      | ❌ No          |
| Controls total namespace usage                     | ❌ No       | ✅ Yes         |
| Sets default requests/limits                       | ✅ Auto     | ❌ No          |
| Prevents unbounded containers                      | ✅ Yes      | ❌ No          |
| Prevents namespace from exceeding cluster capacity | ❌ No       | ✅ Yes         |







