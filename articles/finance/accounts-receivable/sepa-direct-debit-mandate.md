---
title: Nastavení zmocnění přímého inkasa SEPA
description: Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění.
author: ShivamPandey-msft
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bea974750a6ac62d8ddeea5d9d4457f4846cb79
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891631"
---
# <a name="set-up-sepa-direct-debit-mandate"></a>Nastavení zmocnění přímého inkasa SEPA

[!include [banner](../includes/banner.md)]

Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění. Zmocnění, které odběratel podepisuje, opravňuje příjemce k výběru plateb a vydávání příkazů bance odběratele k vyplacení shromážděných prostředků. Tento článek je uspořádán tak, aby zobrazoval proces nastavení zmocnění přímého debetu SEPA.

## <a name="prerequisites"></a>Předpoklady
Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

| Kategorie       | Předpoklad                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Země / oblast | Primární adresa pro právnickou osobu musí být v těchto zemích či oblastech: Belgie, Francie, Itálie, Německo, Nizozemsko, Rakousko nebo Španělsko. |

1. Nastavení číselné řady pro zmocněníy přímého debetu Každý přímý debet musí mít jedinečné číslo. Na stránce **Číselné řady** vytvořte číselnou řadu pro zmocnění k přímému debetu. Tento identifikátor slouží k přiřazení číselné řady k systému zmocnění k přímému debetu na stránce **Parametry pohledávek**.

2. Nastavení parametrů pohledávek pro zmocněníy přímého debetu Na stránce **Parametry pohledávek** nastavte parametry pro zmocněníy přímého debetu. Chcete-li nastavit parametry, na kartě **Přímý debet** změňte výchozí parametry. Poté na kartě **Číselné řady** aktualizujte pole **ID zmocnění přímého debetu** číselnou řadou, kterou jste vytvořili dříve.

3. Nastavení metody platby zmocnění přímého debetu: K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby: Tuto metodu platby použijte u faktur pro generování přímých debetních plateb. Na stránce **Metody platby** nastavte metodu platby. K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:

-   V poli **Typ platby** vyberte možnost **Elektronická platba**.
-   Volitelné: Pokud předpokládáte, že odběratelé mají více zmocnění, vyberte v poli **Období** možnost **Faktura**. Tímto se vytvoří samostatná platba pro každou fakturu, a každá platba bude používat zmocnění, které je určeno pro fakturu.
-   Zvolte možnost **Požadovat zmocnění**, aby se platby vytvářely pomocí zmocnění k přímému debetu. Možnost **Požadovat zmocnění** je k dispozici pouze v případě, že v poli **Typ platby** vyberete možnost **Elektronická platba**.

Další zdroje

[Přehled přímého inkasa SEPA](sepa-direct-debit-overview.md) 

[Vytvoření zmocnění k přímému debetu pro odběratele](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
