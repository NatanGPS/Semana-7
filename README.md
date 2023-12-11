# Semana-7
## Desafio 3: 
<br> 


## Desafio 4:
#Pipeline de Deploy NGINX no GitLab

Este repositório possui uma pipeline de integração contínua (CI) no GitLab que realiza o deploy do servidor NGINX automaticamente quando ocorrem alterações na branch `main`.

## Configuração da Pipeline

A pipeline é configurada no arquivo `.gitlab-ci.yml`. Aqui está um resumo das etapas:

```yaml
stages:
  - deploy

deploy:
  stage: deploy
  script:
    - apt-get update -qy
    - apt-get install -y nginx
    - nginx
  only:
    - main
```


1. **Faça um Fork do Repositório:**
   - Clique no botão "Fork" no canto superior direito desta página para criar uma cópia do repositório em sua conta.

2. **Clone o Repositório:**
   - Clone o repositório forked para a sua máquina local usando o comando:
     ```bash
     git clone https://github.com/seu-usuario/seu-fork.git
     ```

3. **Realize Alterações:**
   - Faça as alterações desejadas no código conforme necessário para o seu projeto.

4. **Commit e Push:**
   - Commit suas alterações e faça push para a branch `main`:
     ```bash
     git add .
     git commit -m "Adicionar novos recursos"
     git push origin main
     ```

5. **Pipeline de CI/CD:**
   - A pipeline será automaticamente acionada no GitLab quando você fizer o push para a branch `main`. Verifique o progresso e os logs na interface web do GitLab em "CI/CD > Pipelines".




