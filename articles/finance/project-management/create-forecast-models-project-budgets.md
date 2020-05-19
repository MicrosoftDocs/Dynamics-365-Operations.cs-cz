---
title: Vytvořte prognózové modely pro rozpočty projektu
description: Toto téma popisuje, jak vytvořit předpovědní model pro zbývající rozpočty.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321772"
---
# <a name="create-forecast-models-for-project-budgets"></a>Vytvořte prognózové modely pro rozpočty projektu 

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit předpovědní model pro zbývající rozpočty. Projekt, který je předmětem kontroly rozpočtu, používá dva typy rozpočtů: původní a zbývající. Při vytváření rozpočtu projektu je nutné zadat modely prognóz původního a zbývajícího rozpočtu, které byly vytvořeny na stránce **Modely prognózy**. Rozpočty projektu založené na zadaných modelech jsou vytvořeny při potvrzení rozpočtu projektu.

> [!NOTE]
> Model prognózy, který se používá pro kontrolu rozpočtu, nemůže obsahovat dílčí model a nelze jej použít jako dílčí model.

1. Vyberte **Řízení a účetnictví projektu** > **Nastavení** > **Prognózy**  > **Modely prognózy**.
2. Vyberte **Nový** k vytvoření nového modelu prognózy. Poté zadejte identifikační číslo a název nového modelu. 
3. Nastavte možnost **Zastaveno** na **Ano**, aby se zabránilo jakýmkoli změnám v liniích prognózy pro model prognózy. 
4. Pokud mají řádky prognózy, s nimiž je spojen model, generovat prognózy cash flow v hlavní knize, nastavte **Zahrnout do prognóz Cash Flow** na **Ano.** 
5. Chcete-li jako datum fakturace použít datum projektu, nastavte **Prognóza data fakturace** na **Ano**. 
6. V poli **Typ rozpočtu** vyberte jednu z následujících typů modelu:

   - **Původní rozpočet**: Tento typ modelu slouží pro původní částky rozpočtu, které jsou potvrzeny, když je původní rozpočet vytvořen a schválen.
   - **Zbývající rozpočet**: Použijte tento typ modelu pro zbývající částky rozpočtu po dobu trvání projektu. Zůstatky v tomto modelu prognózy jsou sníženy o skutečné transakce a sníženy nebo zvýšeny o revize rozpočtu.
   - **Převést do dalšího období**: Tento typ modelu slouží pro převod částek rozpočtu do dalšího období. Převod do dalšího období je volitelný proces, který lze spustit za účelem převedení nevyužitých částek rozpočtu z jednoho fiskálního roku do jiného.

7. Podle potřeby nastavte následující možnosti:

   - Chcete-li jako datum fakturace použít datum projektu, nastavte **Prognóza data fakturace** na Ano.
   - Povolte **Prognóza s WIP** pro prognózu na základě probíhající práce (WIP) a poté vyberte typ WIP. 
   - Můžete ponechat výchozí **Typ rozpočtu** jako **Žádný** nebo zadat nový typ. Typ rozpočtu není možné po změně záznamu změnit.     
    > [!NOTE]
    > Pokud změníte výchozí typ rozpočtu, nebudou žádné další možnosti k dispozici pro aktualizace a tento model prognóz nelze znovu použít. 
   


 

