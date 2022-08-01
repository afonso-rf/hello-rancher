# Chart Hello Rancher

## JackExperts - Kubernetes para estagiarios - Fase 3


## Parâmetros


| Nome                                           | Descrição                                                                                         | Valor                           |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------- |
| `nameOverride`                                 | String para substituir parcialmente o modelo common.names.fullname (manterá o nome da versão)     | `""`                            |
| `fullnameOverride`                             | String para substituir totalmente o modelo common.names.fullname                                  | `""`                            |
| `replicaCount`                                 | Quantidade de replicas desejadas                                                                  | `1`                             |
| `autoscaling.enabled`                          | Habilita o Auto Scaling se colocado em true                                                       | `false`                         |
| `autoscaling.minReplicas`                      | Quantidade minima de replicas no AutoScaling                                                      | `1`                             |
| `autoscaling.maxReplicas`                      | Quantidade maxima de replicas no AutoScaling                                                      | `50`                            |
| `autoscaling.targetCPUUtilizationPercentage`   | Porcentagem de utilização da CPU desejada                                                         | `50`                            |
| `utoscaling.targetMemoryUtilizationPercentage` | Porcentagem de utilização de memória de destino                                                   | `50`                            |
| `pod.annotations`                              | Anotações para pod                                                                                | `{}`                            |
| `pod.imagePullSecrets`                         | Especificar nomes secretos do registro do docker como uma matriz                                  | `[]`                            |
| `pod.securityContext`                          | Contexto de segurança dos pods                                                                    | `{}`                            |
| `pod.nodeSelector`                             | Rótulos de nó para atribuição de pod. Avaliado como um modelo.                                    | `{}`                            |
| `pod.tolerations`                              | Tolerâncias para atribuição de pods. Avaliado como um modelo.                                     | `[]`                            |
| `pod.affinity`                                 | Afinidade para atribuição de pod                                                                  | `{}`                            |
| `image.repository`                             | Repositório de imagens                                                                            | `peteindockerhub/hello-rancher` |
| `image.tag`                                    | Tag de imagem (Se não hover valor, será usado o appVersion como referência)                       | `""`                            |
| `image.pullPolicy`                             | Política de extração de imagem                                                                    | `IfNotPresent`                  |
| `container.port`                               | Define a porta http dentro do contêiner                                                           | `8080`                          |
| `container.protocol`                           | Define o protocolo dentro do contêiner                                                            | `TCP`                           |
| `container.resources`                          | Define os recursos para o contêiner                                                               | `{}`                            |
| `container.securityContext`                    | Definir o contexto de segurança do contêiner                                                      | `{}`                            |
| `probe.liveness.enabled`                       | Ativar livenessProbe                                                                              | `true`                          |
| `probe.liveness.path`                          | Path de apontamento para livenessProbe                                                            | `/`                             |
| `probe.liveness.initialDelay`                  | Segundos de atraso inicial para livenessProbe                                                     | `""`                            |
| `probe.liveness.successThreshold`              | Limite de sucesso para livenessProbe                                                              | `1`                             |
| `probe.liveness.failureThreshold`              | Limite de falha para livenessProbe                                                                | `3`                             |
| `probe.liveness.period`                        | Período em segundos para livenessProbe                                                            | `15`                            |
| `probe.readiness.enabled`                      | Ativar readinessProbe                                                                             | `true`                          |
| `probe.readiness.path`                         | Path de apontamento para readinessProbe                                                           | `/`                             |
| `probe.readiness.initialDelay`                 | Segundos de atraso inicial para readinessProbe                                                    | `""`                            |
| `probe.readiness.successThreshold`             | Limite de sucesso para readinessProbe                                                             | `1`                             |
| `probe.readiness.failureThreshold`             | Limite de falha para readinessProbe                                                               | `3`                             |
| `probe.readiness.period`                       | Período em segundos para readinessProbe                                                           | `10`                            |
| `probe.startup.enabled`                        | Ativar startupProbe                                                                               | `true`                          |
| `probe.startup.path`                           | Path de apontamento para startupProbe                                                             | `/`                             |
| `probe.startup.successThreshold`               | Limite de sucesso para startupProbe                                                               | `1`                             |
| `probe.startup.failureThreshold`               | Limite de falha para startupProbe                                                                 | `10`                            |
| `probe.startup.period`                         | Período em segundos para startupProbe                                                             | `10`                            |
| `service.type`                                 | Tipo de serviço                                                                                   | `ClusterIP`                     |
| `service.port`                                 | Porta HTTP de serviço                                                                             | `80`                            |
| `serviceAccount.create`                        | Habilitar a criação de ServiceAccount para pod                                                    | `false`                         |
| `serviceAccount.annotations`                   | Anotações para conta de serviço. Avaliado como um modelo.                                         | `{}`                            |
| `serviceAccount.name`                          | O nome da ServiceAccount a ser usada.                                                             | `""`                            |
| `ingress.enabled`                              | Defina como true para habilitar a geração de registro de entrada                                  | `false`                         |
| `ingress.className`                            | Defina o ingerssClassName no registro de entrada                                                  | `""`                            |
| `ingress.annotations`                          | Defina como true para habilitar a geração de registro de entrada                                  | `{}`                            |
| `ingress.host`                                 | Host padrão para o recurso de entrada                                                             | `hello-rancher.local`           |
| `ingress.path`                                 | O caminho para a Aplicação. Pode ser necessário configurar como '/*' para usá-lo com entrada ALB. | `/`                             |
| `ingress.pathType`                             | Tipo de caminho de entrada                                                                        | `ImplementationSpecific`        |
| `ingress.tls`                                  | Criar segredo TLS                                                                                 | `[]`                            |
