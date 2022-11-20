<h1 align="center"><img src="./frontend/src/assets/img/banner.svg" width="50"><b> DSMeta</b></h1>

<div align="center">

![alt](https://img.shields.io/badge/java-v17-red?style=flat&logo=coffeescript)
![alt](https://img.shields.io/badge/spring-v2.7.5-green?style=flat&logo=spring)
![alt](https://img.shields.io/badge/npm-v8.19.2-red?style=flat&logo=npm)
![alt](https://img.shields.io/badge/yarn-v1.22.19-blue?style=flat&logo=yarn)
![alt](https://img.shields.io/badge/node-v16.18.1-green?style=flat&logo=nodedotjs)
![alt](https://img.shields.io/github/languages/count/lucasferreiraz/dsmeta)

</div>

<h1 align="center"><img src="./media/desktop.png"></h1>

## About 📚

O **DSMeta** projeto foi desenvolvido durante a 11ª edição do evento Spring React Week** do DevSuperior. Durante o curso, foram abordados os conceitos básicos do framework Spring na construção de endpoints de uma  Rest API no backend e a base React na composição do frontend, colocando tudo em prática no desenvolvimento deste projeto, **DSMeta**. Um serviço fictício que lista as vendas com notificação por SMS.



## Technologies Used 🚀

- Java
- Spring
- Maven
- JPA / Hibernate
- H2 Database
- React JS
- TypeScript
- Axios

As dependências auxiliares podem ser encontradas em: https://github.com/PedroHM06/dsmeta/network/dependencies


## Layout 🔖

O design do projeto **DSMeta** foi baseado no protótipo feito na ferramenta **Figma**, que inclui designs responsivos em outros formatos de tela. O arquivo do navegador pode ser acessado abaixo.
- [Arquivo de desenho do projeto](https://www.figma.com/file/EN1zFtk4eY3Jgmpgi9YaMG/DSMeta1?node-id=0%3A1)


## Endpoints 🔗

Para este projeto foram projetados dois endpoints (clique para expandir): <br>

<details>

<summary><b>Show Sellers:</b> <code>GET localhost/sales</code></summary>

## Show Paginated Sellers List

Returns an object containing a paginated list of the top 20 sellers in the database if the date range is not passed as a parameter in the endpoint call.

**Method** : `GET`

**URL** : `localhost/sales`

### OR

**URL** : `localhost/sales/?minDate=yyyy-MM-dd&maxDate=yyyy-MM-dd`

## Success Response

**Code** : `200 OK`

**Content example:**

```json
{
    "content": [
        {
            "id": 37,
            "sellerName": "Padme",
            "visited": 82,
            "deals": 82,
            "amount": 22465.0,
            "date": "2022-02-27"
        },
        
        "."
        "."
        "."
        
        
        {
            "id": 26,
            "sellerName": "Kal-El",
            "visited": 21,
            "deals": 20,
            "amount": 17126.0,
            "date": "2022-04-03"
        },
        {
            "id": 25,
            "sellerName": "Anakin",
            "visited": 68,
            "deals": 43,
            "amount": 17016.0,
            "date": "2022-04-07"
        }
    ],
    "pageable": {
        "sort": {
            "sorted": false,
            "empty": true,
            "unsorted": true
        },
        "pageNumber": 0,
        "pageSize": 20,
        "offset": 0,
        "paged": true,
        "unpaged": false
    },
    "totalPages": 4,
    "totalElements": 66,
    "last": false,
    "sort": {
        "sorted": false,
        "empty": true,
        "unsorted": true
    },
    "size": 20,
    "number": 0,
    "numberOfElements": 20,
    "first": true,
    "empty": false
}
```
</details>

<details>

<summary><b>Send Notification:</b> <code>GET localhost/sales/{id}/notification</code></summary>

Send the SMS informing the seller's name, total sales value in the month and the date.

**Method** : `GET`

**URL** : `localhost/sales/{id}/notification`

**Code** : `200 OK`

**Content example:**

<h1 align="center"><img src="./media/sms.png" width="400"></h1>

</details>

---

## Demonstration 🖥️

**Retorna uma lista de vendedores com um intervalo de dados.**

![alt](/media/demo1.gif)

**Notificação push sms individual para cada vendedor.**

![alt](/media/demo2.gif)

**O sms é enviado para o número cadastrado no serviço Twilio.**

<img src="./media/sms2.png" width="400">

---

<p align="center" style="font-weight:bolder">
    Desenvolido por  <a href="https://github.com/PedroHM06">Pedro Mota</a>
</p>
