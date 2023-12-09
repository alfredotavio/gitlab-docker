# GitLab e GitLab Runner em Docker Compose

## 🗒️ Descrição
Imagens utilizadas:
* [gitlab](https://hub.docker.com/r/gitlab/gitlab-ce/) - Versão 16.6.1-ce.0
* [gitlab-runner](https://hub.docker.com/r/gitlab/gitlab-runner/) - Versão Alpine

## ◼️ Instalação
Instale o Docker Engine e o Docker Compose seguindo meu guia.

```shell
apt-get update
apt-get install ca-certificates curl gnupg
install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
chmod a+r /etc/apt/keyrings/docker.gpg
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
apt-get update
apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Clone o repositório em seu sistema e inicie a implantação usando Docker Compose.

NOTA: Antes de implantar o Docker Compose, altere a URL de acesso editando o arquivo "docker-compose.yml".
São duas linhas, no atual projeto está definido como gitlab.example.com.

```shell
cd /opt
git clone https://github.com/alfredotavio/gitlab-docker.git
cd gitlab-docker
vim /opt/gitlab-docker/docker-compose.yml
docker compose up -d
```

## 📂 Estrutura:
```shell
.
└── docker-compose.yml
```

## 👨‍💻 Autor
<table>
  <tr>
    <td align="center">
      <a href="#">
        <a href="https://www.linkedin.com/in/alfredotavio/"><img src="https://avatars.githubusercontent.com/u/22720865?v=4" width="100px;" alt="Foto do Alfredo Castro"/><br>
        <sub>
          <b>Alfredo Castro</b>
        </sub>
      </a>
    </td>
  </tr>
</table>
