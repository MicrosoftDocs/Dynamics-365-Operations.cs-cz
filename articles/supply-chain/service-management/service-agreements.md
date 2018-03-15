---
title: "Servisní smlouvy"
description: "Servisní smlouvy vám umožňují definovat zdroje používané při typické servisní návštěvě a způsob, jakým jsou tyto zdroje fakturovány odběrateli."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: cs-cz
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a>Servisní smlouvy

[!include[banner](../includes/banner.md)]


Servisní smlouvy vám umožňují definovat zdroje používané při typické servisní návštěvě a způsob, jakým jsou tyto zdroje fakturovány odběrateli.

Každá servisní smlouva je připojena k projektu, jehož prostřednictvím jsou transakce zaúčtovány a fakturovány. Transakce servisních zakázek lze však fakturovat také přímo prostřednictvím projektu bez nutnosti připojení servisní zakázky k servisní smlouvě. Učinit tak můžete v případě, že je servisní zakázka určena pro jednorázovou servisní návštěvu a nutnost zpracování transakcí servisu rychle převáží nutnost udržovat podrobné informace servisní smlouvy o odběrateli po určitou dobu.

## <a name="service-agreement"></a>Servisní smlouva

V každé servisní smlouvě je nutné zadat projekt, ID servisní smlouvy a skupinu servisní smlouvy. Skupinu servisní smlouvy lze použít k řazení a organizování servisních smluv.

Záhlaví servisní smlouvy obsahuje nastavení, která se vztahují na všechny přiřazené řádky smlouvy:

-  Jedná se o nastavení, které určuje, zda je servisní smlouva pozastavena. Je-li servisní smlouva pozastavena, nelze ze servisní smlouvy generovat servisní zakázky.
-  Jedná se o nastavení trvání servisní smlouvy.
-  Jedná se o nastavení způsobu slučování řádků servisní zakázky do servisních zakázek.
-  Jedná se o nastavení, které určuje, zda je servisní smlouva šablonou.

V záhlaví servisní smlouvy lze dále nastavit všechny předměty servisu a servisní úlohy, které lze použít spolu se servisní smlouvou pomocí zadání konkrétních servisních úloh nebo předmětů servisu, které mají být připojeny k různým řádkům smlouvy.

Ze záhlaví servisní smlouvy lze dále kopírovat řádky servisní smlouvy nebo řádky servisní šablony do aktuální servisní smlouvy.

Je možné pozastavit platnost servisních smluv a zastavit jednotlivé řádky servisní smlouvy.

Jestliže v servisní smlouvě zaškrtnete políčko **Pozastavený**, nebude možné provádět následující akce:

-    Vytvořit servisní zakázky automaticky nebo ručně ze servisní smlouvy.

Jestliže na řádku servisní smlouvy zaškrtnete políčko **Zastaveno**, nebude možné provádět následující akce:

-    Vytvořit servisní zakázky automaticky nebo ručně z řádku servisní smlouvy.
-    Kopírovat řádek servisní smlouvy do jiné servisní smlouvy nebo zakázky.


> [!NOTE]
> Pokud je platnost servisní smlouvy pozastavena, všechny připojené řádky budou zastaveny bez ohledu na stav.

## <a name="service-agreement-lines"></a>Řádky servisní smlouvy

Každý řádek servisní smlouvy podrobně popisuje obsah navrhované servisní práce. Tyto řádky obsahují následující nastavení:

-  Typ transakce a popis typu transakce
-  Zaměstnanec, který provádí servisní práci
-  Předměty, na kterých musí být prováděna pro danou servisní smlouvu
-  Frekvence, s jakou je prováděna daná práce a registrovány přiřazené transakce položek, výdajové transakce a transakce poplatků
-  Časové okno, ve kterém lze seskupit řádky servisní zakázky do servisní zakázky
-  Servisní úlohy používané k seskupení sad řádků smlouvy do pracovních úkolů a k souhrnu pro servisní techniky a odběratele o tom, jaká servisní úloha bude poskytnuta.
-  Jedná se o nastavení, které určuje, zda je řádek ukončen. Je-li řádek ukončen, nelze pro něj vytvářet servisní zakázky.
-  Nastavení projektu, jako je například kategorie a vlastnost řádku

## <a name="related-topics"></a>Související témata

[Vytváření servisních smluv](create-service-agreements.md)
