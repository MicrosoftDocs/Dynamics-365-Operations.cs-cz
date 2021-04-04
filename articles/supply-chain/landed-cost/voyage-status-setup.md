---
title: Nastavení stavu cesty
description: Toto téma popisuje, jak nastavit stavové hodnoty, které mohou uživatelé přiřadit cestám.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500879"
---
# <a name="voyage-status-setup"></a>Nastavení stavu cesty

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Na stránce **Stav plavby** nastavíte stavové hodnoty, které mohou uživatelé přiřadit plavbám. Uživatelé mohou přiřadit hodnoty stavu cesty všem úrovním cesty: cestě, přepravnímu kontejneru, foliu, nákupní objednávce a položce (řádky nákupu a řádky převodní objednávky). Používají se pouze pro dva účely:

- Informujte uživatele o stavu plavby, přepravního kontejneru, folia, nákupní objednávky nebo položky (řádky nákupu a řádky převodní objednávky).
- Omezte použití oblasti nákladů zabráněním úpravám nebo odstranění.

Chcete-li nastavit stavy cesty, přejděte na **Náklady za doručení \> Nastavení \> Stavy cesty**. Můžete zde přidávat, odebírat a upravovat stavy pomocí tlačítek v podokně akcí.

Každá oblast nákladů má vlastní sadu a hierarchii stavů cesty. Proto na stránce **Stav plavby** v poli **Oblast nákladů** musíte nejprve vybrat oblast nákladů, pro kterou chcete zobrazit nebo vytvořit stav cesty. Potom pro každý stav cesty podle potřeby nastavte pole, která jsou popsána v následující tabulce. Všimněte si, že stav cesty lze také automaticky změnit podle systémových událostí, jako jsou pravidla, která byla vytvořena pomocí řídicího centra sledování.

| Pole | popis |
|---|---|
| Stav cesty | Zadejte jméno stavu cesty. |
| popis | Zadejte popis vybraného stavu cesty. |
| Změnit | Toto políčko zaškrtněte, pokud mají uživatelé povoleno upravovat cesty, které mají tento stav. |
| Odstranit | Toto políčko zaškrtněte, pokud mají uživatelé povoleno odstraňovat cesty, které mají tento stav. |
| Povinné | Zaškrtnutím tohoto políčka nastavíte stav cesty jako povinný, aby jej nebylo možné přeskočit. |
| Nadřazená položka | Toto pole slouží k vytvoření hierarchie mezi hodnotami stavu. Stav cesty lze změnit (ručně nebo automaticky) pouze dolů v hierarchii, z nadřazeného stavu na jeden z jejích podřízených stavů.

> [!NOTE]
> Musíte nastavit pouze konkrétní stavy plavby, které vaše organizace používá. Mezi typické stavy plavby patří *Potvrzeno*, *Zboží v přepravě*, *Přijato*, *Připraveno k výpočtu nákladů* a *Vypočítané náklady*. Mohou však existovat i jiné stavy.
