# 📜 Documentação: Resolução de Conflitos no Git

## 📌 Descrição do Conflito

Durante o processo de merge, um conflito surgiu ao tentar unir a branch `feature/semana-03` na branch `main`. O conflito ocorreu no arquivo `Semana-03/README.md`, pois as alterações feitas nas duas branches eram incompatíveis.

### Detalhes do Conflito

1. **Branch `feature/semana-03`**
   - Adição de uma nova descrição na seção da Semana 03 no arquivo `README.md`.

2. **Branch `main`**
   - Modificação da mesma seção no arquivo `README.md` com um conteúdo diferente.

Quando tentamos fazer o merge, o Git detectou que o mesmo trecho do arquivo foi alterado de maneira diferente nas duas branches, resultando em um conflito que precisava ser resolvido manualmente.

## 🛠️ Resolução do Conflito

### Passos para Resolução

1. **Mudança para a branch principal**
   - Primeiro, mudamos para a branch `main`:
     ```bash
     git checkout main
     ```

2. **Atualização da branch principal**
   - Em seguida, atualizamos a branch `main` com as últimas mudanças do repositório remoto:
     ```bash
     git pull
     ```

3. **Tentativa de Merge**
   - Tentamos realizar o merge da branch `feature/semana-03` na branch `main`:
     ```bash
     git merge feature/semana-03
     ```

4. **Identificação e Resolução do Conflito**
   - O Git apresentou um conflito no arquivo `Semana-03/README.md`. O conteúdo conflituoso estava marcado com:
     ```
     <<<<<<< HEAD
     Conteúdo da branch main
     =======
     Conteúdo da branch feature/semana-03
     >>>>>>> feature/semana-03
     ```
   - Editamos o arquivo para combinar as alterações desejadas e removemos as marcações de conflito. O conteúdo final ficou conforme acordado entre as equipes.

5. **Marcação do Conflito como Resolvido**
   - Adicionamos o arquivo ao stage:
     ```bash
     git add Semana-03/README.md
     ```

6. **Commit da Resolução**
   - Completamos o merge com um commit que descreve a resolução do conflito:
     ```bash
     git commit -m "Resolve conflito no README.md da Semana 03"
     ```

7. **Atualização do Repositório Remoto**
   - Por fim, enviamos as mudanças para o repositório remoto:
     ```bash
     git push origin main
     ```

## 📝 Conclusão

O conflito foi resolvido com sucesso, combinando as mudanças das duas branches e garantindo que a descrição da Semana 03 no `README.md` refletisse as atualizações de ambas as branches. As etapas descritas garantiram que o merge fosse completado sem perda de informações e com a integridade dos dados mantida.

**Para mais informações, entre em contato:**  
[LinkedIn](https://www.linkedin.com/in/jhoo-snow/)

