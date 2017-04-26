---
title: "Zaúčtování výroby"
description: "Tento článek obsahuje informace o různých typech účetních zápisů ve výrobním procesu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4a400463c4b84ac8e3e5300bd710fb330458cafd
ms.lasthandoff: 03/31/2017


---

# <a name="production-posting"></a>Zaúčtování výroby

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o různých typech účetních zápisů ve výrobním procesu.

Činnosti zaúčtování výroby následují po výrobních procesech, které jsou popsány v následujících částech.

## <a name="material-consumption"></a>Spotřeba materiálu
Materiály jsou při výrobě registrovány jako spotřebované, když je zaúčtován deník výrobních výdejek. Tento proces generuje výdajové transakce, které se odečtou ze zásob na skladě. V parametrech výroby, můžete určit, zda hodnota surovin, které jsou v průběhu (rozpracované \[NV\]) by měla být zaúčtována do hlavní knihy. Hodnota surovin, které jsou ve výrobě (NV) je pak zaúčtována do vyhrazeného účtu výdejek a stržena z protiúčtu výdejky.

## <a name="time-consumption"></a>Spotřeba času
Čas, který pracovníci stráví na výrobních úlohách, je zaznamenán v deníku karet postupů nebo deníku úkolových lístků. Když tyto deníky jsou zaúčtovány, účtování hlavní knihy do vyhrazeného účtu pro prostředky, které jsou ve výrobě (NV). Toto zaúčtování představuje hodnota času stráveného na výrobní zakázce. Poté, co je výrobní zakázka registrována jako dokončená, jsou vyrovnány účty nedokončené výroby.

## <a name="reporting-finished-goods-and-error-quantities"></a>Hlášení dokončeného zboží a množství chyb
Je-li výrobní zakázka vykázána jako dokončená, jsou v Řízení zásob prostřednictvím Deníku dokončené výroby aktualizována množství dokončeného zboží. Pokud používáte účtování nedokončení výroby (NV), která může být nastavena v parametrech výroby, deník hlavní knihy sníží účty NV a zvýší sklad dokončeného zboží.. Deník používá standardní náklady, které jsou pro produkt definovány.

## <a name="ending-the-production-order"></a>Ukončení výrobní zakázky
Před dokončením výrobní zakázky jsou vypočteny skutečné náklady pro vyrobené množství. Všechny odhadované náklady na materiál, práci a režii jsou stornovány a nahrazeny skutečnými náklady. Celkové náklady na dokončenou položku se zapíší na stranu MD skladového účtu Příjem a na stranu Dal skladového účtu Výdej. Pokud při spuštění výpočtu nákladů zaškrtnete políčko **Koncová práce**, bude stav výrobní zakázky změněn na **Ukončeno**. Nastavení tohoto stavu zabrání tomu, aby k dokončené výrobní zakázce byly nechtěně zaúčtovány další náklady. Můžete určit, že hodnota množství chyb, které jsou hlášeny během hlášení jako dokončené měly být přiděleny správné množství, které jsou hlášeny jako dokončené. Zadáte také, že hodnota množství chyb by měla být účtována do vyhrazeného účtu odpadu.

## <a name="controlling-the-level-of-ledger-posting"></a>Řízení úrovně účtování do hlavní knihy
V nabídce **Parametry modulu řízení výroby**, lze použít pole **Zaúčtování do hlavní knihy** pro nastavení úrovně zaúčtování do hlavní knihy pro výrobní procesy. K dispozici jsou následující hodnoty:

-   **Zboží a prostředek** – Použijte účty hlavní knihy, které se nastavují pro skupiny položek pro suroviny a hotové výrobky. NV pro spotřebu času je převzata z prostředků nebo skupiny prostředků z operací postupů.
-   **Zboží a kategorie** – Použijte účty hlavní knihy, které se nastavují pro skupiny položek pro suroviny a hotové výrobky. NV spotřeby času je převzata z kategorií nákladů, které jsou přiřazeny k operacím postupů.
-   **Skupina účtování výroby** – Použijte účty hlavní knihy, které jsou nastaveny pro výrobní skupiny pro spotřebu materiálu a času. Skupiny účtování výroby jsou přidruženy k uvolněným produktům a zkopírovány do výrobní zakázky při vytvoření objednávky. Zaúčtování výrobních zakázek bude pak probíhat prostřednictvím skupin účtování výroby, které jsou přidruženy k výrobní zakázce.

**Poznámka:** Jestliže byla použita standardní metoda výpočtu nákladů na dokončenou položku, projeví se tento fakt i ve výsledných transakcích. Jestliže je rozdíl mezi skutečnými náklady a náklady vypočtenými standardní metodou, tento rozdíl se zaúčtuje na účet vykazující zisk nebo ztrátu.




