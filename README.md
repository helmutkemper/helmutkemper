# Presentation (English):

I am [**Helmut Kemper**](https://www.linkedin.com/in/helmut-kemper-93a5441b/) and I am a specialist developer with about 5 years of experience in Golang and more than 20 years of professional experience.

I started programming in assembly of the [80C51, Intel](https://www.nxp.com/docs/en/data-sheet/8XC51_8XC52.pdf) microcontroller back in the late 1990s and fell in love with hardware. Then life took me to [PHP](https://www.php.net/), [MongoDB](https://www.mongodb.com/), [Open Street Maps](https://www.openstreetmap.org/), [Docker](https://www.docker.com/), [gRPC](https://grpc.io/) and a host of other technologies.

#### **C** is life! **Golang** is an evolution of **C**!

![Valchan's github stats](https://github-readme-stats.vercel.app/api?username=helmutkemper&show_icons=true)

# Apresentação (Português):

Meu nome é [**Helmut Kemper**](https://www.linkedin.com/in/helmut-kemper-93a5441b/), sou desenvolvedor especialista **[Golang](https://golang.org/)** na **[TC](https://tc.com.br/)**.

Caso você esteja começando em [Golang](https://golang.org/), mas, já saiba programar, [**essa Wiki**](https://github.com/helmutkemper/golang.solid.kiss.complexity.measure/wiki) é minha contribuição para você.

Nela você poderá encontrar uma série de textos sobre como programar em [Golang](https://golang.org/) e como evitar alguns erros.

## Sobre mim

Comecei a programar em assembly do [80C51](https://www.nxp.com/docs/en/data-sheet/8XC51_8XC52.pdf), microcontrolador da Intel lá pelo final da década de 1990 e me apaxonei por hardware. Depois a vida me levou para [PHP](https://www.php.net/), [MongoDB](https://www.mongodb.com/), mapas do [Open Street Maps](https://www.openstreetmap.org/), [Docker](https://www.docker.com/), [gRPC](https://grpc.io/) e uma infinidade de outras tecnologias.

Por isto, fique de olho na [Wiki](https://github.com/helmutkemper/golang.solid.kiss.complexity.measure/wiki), e aos poucos eu vou adicionando mais esperiências e códigos para serem compartilhados com a comunidade **Open Source**.

## Agradecimento especial

O profissional que eu sou hoje tem uma influência muito grande de todos os meus professores, amigos e colegas de trabalho, mas, uma pessoa se destacou em todos esses anos, meu amigo e mentor [**Abner Barros**](https://www.linkedin.com/in/abner-barros-5b86409/). Sem ele, eu não teria chegado aqui!

**Obriado Hômí!**

#### **C** é vida! **Golang** é a evolução do **C**!

## Personal projects / Projetos pessoais


### docker builder

[**https://github.com/helmutkemper/iotmaker.docker.builder**](https://github.com/helmutkemper/iotmaker.docker.builder)

<p>
  <a href="https://goreportcard.com/report/github.com/helmutkemper/iotmaker.docker.builder">
    <img src="https://goreportcard.com/badge/github.com/helmutkemper/iotmaker.docker.builder">
  </a>
</p>

**English:** Golang and docker made simple

**Português:** Golang e docker de uma forma simples

```golang
var mongoDocker = &ContainerBuilder{}
// set an image name
mongoDocker.SetImageName("mongo:latest")
// set a container name
mongoDocker.SetContainerName("container_delete_mongo_after_test")
// set a port to expose
mongoDocker.AddPortToOpen("27017")
// se a environment var list
mongoDocker.SetEnvironmentVar(
  []string{
    "--host 0.0.0.0",
  },
)
// set a MongoDB data dir to ./test/data
err = mongoDocker.AddFiileOrFolderToLinkBetweenConputerHostAndContainer("./test/data", "/data")
if err != nil {
  panic(err)
}

// set a text indicating for container ready for use
mongoDocker.SetWaitStringWithTimeout(
  `"msg":"Waiting for connections","attr":{"port":27017`,
  20*time.Second,
)
// inicialize the object before sets
err = mongoDocker.Init()
if err != nil {
  panic(err)
}

// build a container
err = mongoDocker.ContainerBuildFromImage()
if err != nil {
  panic(err)
}

// At this point, the MongoDB is ready for use on port 27017
```

### docker

[**https://github.com/helmutkemper/iotmaker.docker**](https://github.com/helmutkemper/iotmaker.docker)

<p>
  <a href="https://goreportcard.com/report/github.com/helmutkemper/iotmaker.docker">
    <img src="https://goreportcard.com/badge/github.com/helmutkemper/iotmaker.docker">
  </a>
  <a href="https://pkg.go.dev/github.com/helmutkemper/iotmaker.docker/v1.0.0?tab=doc">
    <img src="https://github.com/helmutkemper/iotmaker.docker/blob/master/image/godoc.svg">
  </a>
</p>

**English:** Container manager by line of **Golang** code.
It allows any developer **Golang** to create and manage containers in a simple and documented way by code.

**Português:** Gerenciador de containers por linha de código **golang**.
Permite a qualquer desenvolvedor **golang** criar e gerenciar container de forma simples e documentada por código. 

<!--
**helmutkemper/helmutkemper** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
