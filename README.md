• Por que a Secret aparece no log como ** e a variável aparece
normalmente?
R: No github automaticamente oculta o secrets nos logs, para prevenir a exposição de senhas e tokens sensíveis. 
Variáveis não têm esse cuidado, pois não são dados sensíveis.

• O Job deploy_app consegue ler a variável BUILD_VERSION criada no Job
build_app? Por quê?
R: Não. Cada Job é executado em um runner isolado e diferente.
Variáveis de ambiente definidas no escopo de um job não são compartilhadas com outros jobs por padrão
