---
title: Typy kritičnosti majetku
description: Téma vysvětluje typy kritičnosti majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7d6e3dea1b3c1ef47490df678f639c036cdd5c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423723"
---
# <a name="asset-criticality-types"></a>Typy kritičnosti majetku

[!include [banner](../../includes/banner.md)]

 

Téma vysvětluje typy kritičnosti majetku v modulu Správa majetku. Kritičnost majetku se vztahuje k majetku a je převedena na pracovní příkazy. Nelze ji změnit v pracovním příkazu. Kritičnost majetku se používá k výpočtu kritičnosti pracovního příkazu během plánování pracovního příkazu. Jinými slovy, používá se k výpočtu míry, do jaké ovlivňuje práce údržby na majetku plán výroby a produktivitu vaší firmy. Další informace o nastavení, které souvisí s výpočtem skóre hodnocení pro plánování pracovních příkazů, naleznete v tématu [Parametry Správy majetku](../setup-for-objects/enterprise-asset-management-parameters.md).

Chcete-li nastavit kritičnost, nejprve vytvořte typy kritičnosti, které by měly být použity v nastavení majetku. Potom nastavíte kritičnost majetku.

## <a name="set-up-criticality-types"></a>Nastavit typy kritičnosti

1. Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Typy kritičnosti**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Kritičnost** zadejte číslo označující kritičnost.
4. V poli **Název** zadejte název typu kritičnosti.
5. Do pole **Faktor** zadejte faktor. Tento faktor se používá při výpočtu plánování pracovních příkazů k určení záznamu kritičnosti, který by měl být použit. (Záznam s nejvyšším faktorem je vždy použit.) Toto nastavení je důležité, pokud, jak je znázorněno na následujícím obrázku, jsou vytvořeny řádky kritičnosti, které mají stejnou hodnotu kritičnosti.

    ![Stránky Typy kritických záležitostí](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Nastavení kritičnosti majetku

1. Vyberte **Správa majetku** \> **Nastavení** \> **Kritičnost majetku**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. V závislosti na požadované úrovni podrobností o majetku proveďte příslušné výběry v polích **Funkční umístění**, **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Kategorie typu práce**, **Typ práce**, **Varianta typu práce** a **Požadavek na práci**.

    > [!NOTE]
    > Pokud je vybrána kritičnost majetku, projde Správa majetku všemi záznamy o kritičnosti majetku, aby mohla zkontrolovat možnou shodu. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, Správa majetku nejprve zkontroluje **Požadavek na práci**. Není-li nalezena shoda, kontroluje **Varianta typu práce**. Není-li nalezena shoda, kontroluje **Typ práce** a tak dále. Jak vidíte v rozvržení stránky, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody. Není-li nalezena shoda, použije se "výchozí" záznam, který nemá žádné výběry.

4. V poli **Kritičnost** vyberte jednu z hodnot kritičnosti, které jste vytvořili v předchozích krocích.

### <a name="notes-about-criticality-setup"></a>Poznámky o nastavení kritičnosti

- Změníte-li v tomto nastavení kritičnost majetku poté, co jste jej již použili v pracovním příkazu, nebude tato kritičnost v pracovním příkazu odpovídajícím způsobem aktualizována.
- Kritičnost na pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.
- Pokud pracovní příkaz obsahuje několik prací pracovního příkazu, v pracovním příkazu je vždy použita nejvyšší kritičnost podle pole **Faktor** na stránce **Typy kritičnosti**.
- Obecně platí, že kritičnost majetku se může v průběhu období změnit. Kritičnost může být ovlivněna nákupem nového vybavení, rekonstrukcí a tak dále. Zvažte možnost přehodnocením kritičnosti svého majetku v pravidelných intervalech (například jednou za rok nebo každý druhý rok), abyste zajistili, že se vaše definice kritičnosti shodují s aktuálním nastavením výroby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]