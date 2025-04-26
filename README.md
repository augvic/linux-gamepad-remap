# 📦 Remap de controle para funcionar 100% no Linux

Este guia explica como fazer remap de controles (gamepad) para ficar funcional no Linux, caso o mapeamento padrão esteja incorreto.

---

## ✅ 1. Instalar o AntiMicroX

```bash
sudo dnf install antimicrox
```

Ou baixe as versões ".rpm" e "flatpack" da loja. 

---

## ✅ 2. Dentro do AntiMicroX

1 - Plugue o controle.

2 - Abra o AntiMicroX e vá na opção "Controller Mapping".

3 - Faça o mapeamento do controle na tabela de "Mapping".

4 - Copie a string no output abaixo da tabela.

---

## ✅ 3. Exportando o mapeamento para o sistema

1 - Execute o comando:

```bash
nano .bashrc
```

2 - Ao final do arquivo, adicione:

`export SDL_GAMECONTROLLERCONFIG="<string_de_mapeamento>"`

3 - "CTRL+O" e "ENTER" para salvar e "CTRL+X" para sair.

4 - Recarregue o "bashrc":

```bash
source ~/.bashrc
```

---

## ✅ 4. Verificar o UUID

```bash
sudo blkid /dev/<partição>
```

Anote o valor do `UUID`.

---

## ✅ Pronto!

O mapeamento foi feito corretamente. Se necessário, reinicie e boa diversão!