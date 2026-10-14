# Duelo dos Números — site e política de privacidade

Site estático sem dependências. Abra `dist/index.html` ou sirva a pasta `dist` com um servidor HTTP. A política está em `dist/privacidade.html`; o link direto para exclusão é `privacidade.html#exclusao`.

## Estado

Página visual implementada; política em revisão e não vigente. Não cadastrar a prévia privada na Google Play. A política final precisa estar em URL pública HTTPS, sem login, restrição geográfica ou edição por visitantes, acessível também dentro do app. Não basta publicar este texto para garantir conformidade.

## Pendências concretas para finalizar

- Confirmar nome/razão social do controlador e e-mail real de privacidade. Fernando Castro consta nos créditos, mas a identidade jurídica do controlador não foi inferida.
- Confirmar público-alvo e implementar controles aplicáveis a menores/Famílias.
- Implementar exclusão dentro do app e atendimento externo funcional. Não foi localizada função de exclusão de conta no código examinado. Apagar autenticação isoladamente não remove Firestore, histórico, backups etc.
- Definir períodos por categoria, exceções legais, backups e prazo operacional de exclusão; validar rotina efetiva no backend.
- Confirmar bases legais, fornecedores, regiões e salvaguardas de transferência internacional.
- Validar SDK de anúncios e consentimento antes da inicialização/coleta quando necessário; IDs atuais são de teste. Não há garantia de ausência de coleta com anúncios de teste.
- Conferir dados e compartilhamentos no binário de produção e preencher Segurança dos dados no Play Console de forma consistente, inclusive dados coletados por SDKs.
- Revisar regras do Firestore, permissões reais do Android e proteção de informações de perfil. Esta tarefa não auditou segurança do backend.
- Confirmar hospedagem e logs. Após resolver as pendências, substituir trechos provisórios, retirar o aviso de revisão e atualizar a data de vigência. `noindex` não bloqueia acesso, mas pode ser removido na versão final.

## Evidências locais

Projeto consultado: `C:/Games/duelo-dos-numeros-game`, versão 1.0.25, pacote `com.duelodosnumeros.game`. Fontes: `app.json`, `package.json`, `src/services/firebase/types.ts`, `firebaseClient.native.ts`, `src/services/ads.ts`, `src/features/ads/policy.ts`, `src/config/releaseFeatures.ts`, telas de créditos e traduções. Nenhum arquivo do jogo foi alterado. Marca e cores copiadas dos recursos originais.

## Referências oficiais

- https://support.google.com/googleplay/android-developer/answer/10144311?hl=pt-BR
- https://support.google.com/googleplay/android-developer/answer/13327111?hl=pt-BR
- https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709compilado.htm
- https://developers.google.com/admob/android/privacy/play-data-disclosure
- https://www.gov.br/anpd/pt-br/assuntos/noticias/anpd-divulga-enunciado-sobre-o-tratamento-de-dados-pessoais-de-criancas-e-adolescentes
