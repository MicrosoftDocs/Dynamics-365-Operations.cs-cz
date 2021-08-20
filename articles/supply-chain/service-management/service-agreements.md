---
title: Přehled přípravy a zřízení servisních smluv
description: Servisní smlouvy vám umožňují definovat zdroje používané při typické servisní návštěvě a způsob, jakým jsou tyto zdroje fakturovány odběrateli.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e90161e7fa599fc76013277d3c80919fc144b77d3477e5d0318bdb5ef6da422c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771244"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Přehled přípravy a zřízení servisních smluv

[!include [banner](../includes/banner.md)]

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]