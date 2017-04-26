---
title: "Nastavení zmocnění přímému debetu SEPA"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Nastavení zmocnění přímému debetu SEPA

[!include[banner](../includes/banner.md)]




Přímý debet SEPA (Jednotná oblast pro platby v eurech) umožňuje příjemci vybírat finanční prostředky z bankovního účtu odběratele za předpokladu, že odběratel udělil příjemci podepsané zmocnění. Zmocnění, které odběratel podepisuje, opravňuje příjemce k výběru plateb a vydávání příkazů bance odběratele k vyplacení shromážděných prostředků. V tomto tématu jsou uspořádány k zobrazení procesu nastavení pověření pro přímý debet SEPA.

## <a name="prerequisites"></a>Předpoklady
Následující tabulka zobrazuje požadavky, které musí být splněny, než začnete.

| Kategorie       | Předpoklad                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Země / oblast | Primární adresa pro právnickou osobu musí být v těchto zemích či oblastech: Belgie, Francie, Itálie, Německo, Nizozemsko, Rakousko nebo Španělsko. |

1. Nastavte číselnou řadu pro přímý debet pověření každý přímý debet pověření musí mít jedinečné číslo. Na stránce **Číselné řady** vytvořte číselnou řadu pro zmocnění k přímému debetu. Tento identifikátor slouží k přiřazení číselné řady k systému zmocnění k přímému debetu na stránce **Parametry pohledávek**.

2. Nastavení parametrů pohledávek pro přímý debet pověření použít **parametry pohledávek** stránku lze nastavit parametry pro přímý debet pověření. Chcete-li nastavit parametry, na **přímého debetu** karta, potřebujete změnit výchozí parametry. Poté na **číselné řady** tab, aktualizovat **ID přímého debetu mandát** pole s číselnou řadu, kterou vytvořili dříve.

3. Nastavit metodu platby pro přímý debet vyžaduje, je nutné nastavit metodu platby pro přímý debet pověření. Tuto metodu platby použijte u faktur pro generování přímých debetních plateb. Na stránce **Metody platby**nastavte metodu platby. K nastavení metody platby pro zmocnění k přímému debetu je nutné provést následující kroky pro metodu platby:

-   V poli **Typ platby** vyberte možnost **Elektronická platba**.
-   Volitelné: Pokud očekáváte, že každý z vašich zákazníků mít více ukládá, v **období** pole: vyberte **fakturace**. Vytvoří se samostatnou platbu pro každou fakturu a každou platbu použije pověření, která je určena pro fakturu.
-   Zvolte možnost **Požadovat zmocnění**, aby se platby vytvářely pomocí zmocnění k přímému debetu. Možnost **Požadovat zmocnění** je k dispozici pouze v případě, že v poli **Typ platby** vyberete možnost **Elektronická platba**.

Viz také [přehled přímého debetu](sepa-direct-debit-overview.md) 



