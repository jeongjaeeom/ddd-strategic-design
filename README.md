# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

### 공통

| 한글명 | 영문명       | 설명                                 |  
|-----|-----------|------------------------------------|  
| 비속어 | Profanity | 비속어를 의미한다. 욕설 또는 불편한 단어를 포함할 수 있다. |

### 상품(Product)

| 한글명  | 영문명     | 설명 |  
|------|---------| --- |  
| 상품   | Product | 상품은 판매할 음식이다. 단독적으로 판매할 수 없고, 하나 이상의 메뉴에 포함된다.  |
| 상품ID | ID      |  상품을 유일하게 식별할 수 있는 식별자이다. |
| 상품명  | Name    |  상품의 이름이다. |
| 상품가격 | Price   |  상품의 가격이다. |

### 메뉴그룹(MenuGroup)

| 한글명  | 영문명        | 설명 |  
|---|------------| --- |  
| 메뉴그룹 | Menu Group | 메뉴를 분류하기 위한 그룹이다. 메뉴그룹은 하나 이상의 메뉴를 포함한다. |
| 메뉴그룹ID | ID         |  메뉴그룹을 유일하게 식별할 수 있는 식별자이다. |
| 메뉴그룹명 | Name       | 메뉴그룹의 이름이다. |

### 메뉴(Menu)

| 한글명    | 영문명            | 설명                                      |  
|--------|----------------|-----------------------------------------|  
| 메뉴     | Menu           | 메뉴는 한 개 이상의 메뉴 상품으로 구성되어 판매되는 항목이다.     |
| 메뉴ID   | ID             | 메뉴를 유일하게 식별할 수 있는 식별자이다.                |
| 메뉴명    | Name           | 메뉴의 이름이다.                               |
| 메뉴가격   | Price          | 메뉴의 가격이다. 메뉴의 가격은 메뉴상품들의 가격과 같거나 적어야 한다. |
| 공개     | Display        | 메뉴를 공개하는 것을 의미한다.                       |.
| 공개된 메뉴 | Displayed Menu | 메뉴가 공개되어 판매 가능한 메뉴이다.                   
| 비공개 | Hide           | 메뉴를 비공개하는 것을 의미한다.                      |
| 비공개된 메뉴 | Hidden Menu    | 메뉴가 비공개되어 판매 불가능한 메뉴이다.                 |
| 메뉴상품   | Menu Product   | 메뉴에 포함된 상품이다. 메뉴는 한개 이상의 상품을 포한한다.      |

### 매장주문(EatInOrder)

| 한글명   | 영문명            | 설명                                                |  
|-------|----------------|---------------------------------------------------|  
| 주문    | Order          | 매장 주문은 고객이 매장에서 식사를 하기 위해 종업원에게 음식을 요구하는 것을 의미한다. |
| 주문ID  | ID             | 매장 주문을 유일하게 식별할 수 있는 식별자이다.                       |
| 주문상태  | Order Status   | 매장 주문의 진행 상태이다. '대기 중', '접수됨', '제공됨', '주문완료'가 있다. |
| 주문시간  | Order Date Time | 매장 주문이 발생한 시간이다.                                  |
| 주문상품  | Order Line Item | 매장 주문 메뉴와 수량에 대한 정보이다. 주문은 하나 이상의 주문상품을 포함한다.     |
| 주문접수  | Accept         | 매장 손님의 주문을 접수하는 것이다.                              |
| 접수된 주문 | Accepted Order      | 매장 주문이 접수된 주문을 의미한다.                              |
| 서빙    | Serve          | 매장 손님에게 음식을 제공하는 것이다.                             |
| 서빙된 주문 | Served Order        | 매장 손님에게 음식이 제공된 주문을 의미한다.                         |
| 주문완료  | Complete       | 매장 주문을 완료하는 것이다.                                  |
| 완료된 주문 | Completed Order| 매장 주문이 완료된 주문을 의미한다.                              |

### 포장주문(TakeoutOrder)

| 한글명   | 영문명             | 설명                                                   |  
|-------|-----------------|------------------------------------------------------|  
| 주문    | Order           | 포장 주문은 고객이 매장 외부에서 음식을 소비하기위해 음식 포장을 요구하는 것을 의미한다.   |
| 주문ID  | ID              | 포장 주문을 유일하게 식별할 수 있는 식별자이다.                          |
| 주문상태  | Order Status    | 포장 주문의 주문 진행 상태이다. '대기 중', '접수됨', '제공됨', '주문완료'가 있다. |
| 주문시간  | Order Date Time | 포장 주문이 들어온 시간이다.                                     |
| 주문상품  | Order Line Item | 포장 주문한 메뉴와 수량에 대한 정보이다. 주문은 하나 이상의 주문상품을 포함한다.       |
| 주문접수  | Accept          | 포장 고객의 주문을 접수하는 것이다.                                 |
| 접수된 주문 | Accepted Order  | 포장 주문이 접수된 주문을 의미한다.                                 |
| 포장준비  | Serve           | 포장 주문 음식을 준비하는 것이다.                                  |
| 준비된 주문 | Served Order         | 포장 주문 음식이 준비된 주문을 의미한다.                              |
| 주문완료  | Complete        | 포장 주문을 완료하는 것이다.                                     |
| 완료된 주문 | Completed Order      | 포장 주문이 완료된 주문을 의미한다.                                 |

### 배달주문(DeliveryOrder)

| 한글명    | 영문명                | 설명                                                                   |
|--------|--------------------|----------------------------------------------------------------------|  
| 주문     | Order              | 배달 주문은 고객이 고객의 배송지로 음식 배달을 요구하는 것을 의미한다.                             |
| 주문ID   | ID                 | 배달 주문을 유일하게 식별할 수 있는 식별자이다.                                          |
| 주문상태   | Order Status       | 배달 주문의 주문 진행 상태이다. '대기 중', '접수됨', '제공됨', '배달 중', '배달완료', '주문완료'가 있다. |
| 주문시간   | Order Date Time    | 배달 주문이 들어온 시간이다.                                                     |
| 주문상품   | Order Line Item    | 배달 주문한 메뉴와 수량에 대한 정보이다. 주문은 하나 이상의 주문상품을 포함한다.                       |
| 주문접수   | Accept             | 배달 주문 고객의 주문을 접수하는 것이다.                                              |
| 접수된 주문 | Accepted Order     | 배달 주문이 접수된 주문을 의미한다.                                                 |
| 배달 대행사 | Delivery Agency    | 배달 주문을 배달해주는 배달 대행사이다.                                               | 
| 요청된 배달 | Requested Delivery | 배달 대행사에게 요청된 배달을 의미한다.                                               |
| 준비된 주문 | Served Order       | 배달 주문에 대한 음식이 준비된 것을 의미한다.                                           |
| 배달시작   | Delivering Order   | 배달 중인 주문을 의미한다.                                                      |
| 배달완료   | Complete Delivery  | 고객에게 배달이 완료된 것을 의믜한다.                                                |
| 완료된 주문 | Completed Order    | 배달 주문이 완료된 것을 의미한다.                                                  |

### 주문테이블(OrderTable)

| 한글명   | 영문명              | 설명 |  
|-------|------------------| --- |  
| 주문테이블 | Order Table      | 매장 손님들이 앉아서 식사 가능한 매장 테이블이다. |
| 주문테이블명 | Name             | 주문테이블의 이름이다. |
| 손님 수  | Number Of Guests | 주문테이블에 앉은 손님들의 수다. |
| 사용 여부 | Occupied         | 주문테이블 사용 여부를 나타낸다. |

## 모델링

### 상품(Product)
#### 속성
* `상품(Product)`은 유일하게 식별 가능한 `식별자(ID)`를 가진다.
* `상품(Product)`은 상품의 이름인 `상품명(Name)`을 가진다.
  * `상품명(Name)`은 없거나 비어있을 수 없다.
  * `상품명(Name)`은 `비속어(Profanity)`를 포함할 수 없다.
* `상품(Product)`은 상품의 가격인 `상품가격(Price)`을 가진다.
  * `상품가격(Price)`은 0보다 큰 값을 가져야 한다.
  
#### 행위
* `상품(Product)`을 등록 할 수 있다. 
* `상품(Product)`의 `상품가격(Price)`을 변경할 수 있다.
  * `상품가격(Price)`이 변경되면 상품가격변경 이벤트를 발행한다.
* `상품(Product)`을 조회할 수 있다.
