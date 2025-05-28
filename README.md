# 💻 Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure 🚀

Fala, dev! 👋

Se você tá começando a explorar o mundo da **Azure** e caiu de paraquedas tentando entender como **criar e configurar uma VM (Máquina Virtual)**, esse repositório é pra você. Aqui eu destrincho o básico (e o não tão básico assim) sobre:

- Como criar sua primeira VM no Azure
- Escolher os tamanhos certos (e não gastar grana à toa)
- Subir containers dentro da VM (porque sim, container também é vida!)
- Dicas de escalabilidade e performance 🧠

> 💡 Objetivo: Te ajudar a entender **como dimensionar e configurar VMs no Azure de forma prática**, do zero até o deploy de algo útil rodando. Sem enrolação!

---

## 🧱 1. O que é uma VM no Azure?

Pensa numa VM como um computador dentro da nuvem. Você escolhe o sistema operacional, CPU, memória, e até a região do planeta onde ela vai rodar. Com VMs, você pode:

- Rodar apps legacy que ainda dependem de um servidor "clássico"
- Criar labs de teste
- Subir um ambiente de dev ou staging
- Rodar containers com mais controle (e sem Kubernetes, se quiser algo mais simples)

---

## ⚙️ 2. Como criar uma VM passo a passo

Tem tutorial completo aqui na pasta [`/vm-basics`](./vm-basics), mas o resumo é:

1. Entra no portal do Azure
2. Vai em **Máquinas Virtuais > Criar**
3. Escolhe:
   - Imagem (Ubuntu, Windows, etc.)
   - Tamanho (B1s, D2s, etc.)
   - Autenticação (senha ou chave SSH)
4. Cria e BOOM 💥, sua VM tá de pé!

---

## 📏 3. Dimensionando recursos (CPU, memória e disco)

Aqui é onde a grana pode sumir se você não prestar atenção.

- **B-series**: boas pra dev/teste, baratas.
- **D-series**: equilibradas pra apps de produção leve/média.
- **F/G/H-series**: potência bruta ($$$) pra cargas pesadas.

Além disso:
- Use discos gerenciados Standard_LRS pra economizar.
- Monitoramento ativo (com Azure Monitor) evita surpresas.

---

## 🐳 4. Rodando containers dentro da VM

Sim! Você pode rodar **Docker** numa VM tranquilamente.

```bash
sudo apt update
sudo apt install docker.io
sudo systemctl start docker
sudo docker run hello-world

````

-----

📈 5. Escalabilidade: manual x automática
Escalabilidade vertical: trocar a VM por uma maior.

Escalabilidade horizontal: criar várias VMs e distribuir a carga (usando VM Scale Sets, por exemplo).

Protip: Usa Auto-shutdown e Auto-scale pra não pagar além do necessário. 😉

🧪 6. Extras (porque ninguém vive só de teoria)
Exemplo de container + banco de dados dentro da VM

Scripts de automação com Azure CLI

Dicas de segurança (NSG, SSH, etc.)

Como usar Azure Container Instances (ACI) se não quiser usar VM

🤓 Curtiu?
Se esse repositório te ajudou, deixa uma ⭐ aí pra eu saber que tô no caminho certo!

Pull requests são bem-vindos — bora melhorar isso juntos!

Feito com café ☕ e curiosidade por alguém tentando dominar a nuvem.

