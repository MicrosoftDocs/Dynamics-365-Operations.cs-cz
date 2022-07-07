---
title: Hodnocení stavu
description: Tento článek vysvětluje, jak vytvořit šablonu hodnocení podmínky a registraci majetku v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c43424a0955d7a046186e8a4120c050990df6060
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015049"
---
# <a name="condition-assessment"></a>Hodnocení stavu

[!include [banner](../../includes/banner.md)]

 

Tento článek vysvětluje, jak vytvořit šablonu hodnocení podmínky a registraci majetku v modulu Správa majetku. Vyhodnocení stavu se provádí v pravidelných intervalech a primárním cílem je vytvořit a udržovat údaje o stavu majetku. Z hlediska preventivní údržby je důležité sledovat klíčové informace, jako je aktuální stav a zbývající životnost. Dále, pokud budete provádět hodnocení stavu v pravidelných intervalech, budete moci monitorovat a porovnávat podmínky strojního zařízení ve vaší továrně.

Posouzení podmínek lze použít k měření a sledování mnoha podmínek vašeho zařízení. Příklad: můžete měřit vibrace vašeho strojního zařízení. Poté, co jste zaregistrovali měření vibrací v modulu Správa majetku u různých typů zařízení, můžete vyhledat nejnovější registrované hodnocení a zobrazit měření vibrací.

Vyhodnocení podmínek se vytváří u majetku. Před provedením postupu posouzení podmínek nastavíte pro typ majetku šablonu zhodnocení stavu. Důvodem pro použití šablon pro posouzení stavu je zamezit změnám dat o podmínkách podobného majetku. Posloupnost pro nastavení a použití vyhodnocení podmínek v modulu Správa majetku je: nejprve nastavte požadované šablony vyhodnocení podmínek. Dále přidružíte šablony k typům majetku ve formuláři **Typy majetku**. Nakonec můžete vytvořit registrace vyhodnocení podmínky u majetku ve formuláři **Majetek**.

## <a name="create-a-condition-assessment-template"></a>Vytvoření šablony vyhodnocení podmínek

1. Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Vyhodnocení podmínek**.
2. Zvolte **Nový** pro vytvoření nové šablony.
3. V poli **šablona** zadejte ID šablony.
4. Do pole **Název** zadejte název šablony.
5. Na pevné záložce **Řádky hodnocení podmínky** přidejte řádky požadované pro posouzení podmínky, včetně výběru příslušného typu podmínky a měrné jednotky.
6. Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly používat šablonu vyhodnocení podmínky.
7. V polích **Řádky** a **Typy majetku** skupiny **Detaily** v horní části obrazovky uvidíte počet řádků hodnocení a typy majetku související s vybranou šablonou hodnocení podmínky.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Vytvoření registrace vyhodnocení podmínky u majetku

1. Vyberte **Správa majetku** > **Majetek** > **Všechen majetek**.
2. V seznamu vyberte majetek, pro který chcete vytvořit registraci hodnocení majetku.
3. Na kartě **obecné** klepněte na tlačítko **vyhodnocení podmínky**.
4. Kliknutím na **Nový** vytvořte novou registraci.
5. V poli **datum** vyberte datum pro vyhodnocení podmínky.
6. Vyberte jméno pracovníka, který provedl registraci vyhodnocení v poli **pracovník**.
7. V poli **řádky** uvidíte počet řádků vyhodnocení nastavených pro vyhodnocení podmínky.
8. V poli **šablona** vyberte šablonu pro vyhodnocení podmínky. Název šablony je automaticky vložen do pole **název** a související řádky registrace se vloží na pevnou záložku **řádky vyhodnocení podmínky**.
9. Můžete vložit poznámky vztahující se k vybranému vyhodnocení podmínky na pevné záložce **Poznámky**.
10. Pro každý řádek hodnocení podmínek vložte data měření do pole **hodnota**.
11. Můžete vložit poznámku vztahující se k vybranému řádku registrace na pevné záložce **řádky vyhodnocení podmínky** > **poznámky**. Pokud přidáte komentář k řádku, bude automaticky zaškrtnuto políčko **Komentář**.

Po provedení registrace pro zhodnocení stavu majetku můžete vytisknout sestavu vyhodnocení podmínek.

>[!NOTE]
>Vyhodnocení podmínky můžete také zaregistrovat v pracovním příkazu (tlačítko **Správa majetku** > **Pracovní příkazy** > **Všechny pracovní příkazy** > **Vyhodnocení podmínky**.)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]