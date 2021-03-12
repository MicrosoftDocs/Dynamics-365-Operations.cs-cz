---
title: Workflow dodavatele
description: Upravte informace o dodavateli a použijte k jejich schválení workflow.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1fad41fa4fb3562ab94adde522d3899271c85467
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979157"
---
# <a name="vendor-workflow"></a>Workflow dodavatele

[!include [banner](../includes/banner.md)]

Při použití workflow dodavatele jsou změny určitých polí odeslány do workflow ke schválení před tím, než jsou přidány k dodavateli.

## <a name="set-up-the-vendor-workflow"></a>Nastavení workflow dodavatele

Než budete funkci workflow moci používat, musíte ji povolit.

1. Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
2. Na kartě **Obecné** na pevné záložce **Schválení dodavatele** nastavte možnost **Povolit schválení dodavatele** na **Ano**.
3. V poli **Chování datových entit** vyberte chování, které chcete použít při importu dat:

    - **Povolit změny bez schválení** – datová entita může aktualizovat záznam dodavatele bez jeho zpracování přes workflow.
    - **Odmítnout změny** – změny záznamu dodavatele nelze provést. Import se nezdaří u polí, která jsou povolena pro workflow.
    - **Vytvořit návrhy změny** – všechna pole se změní, kromě polí, která jsou povolena pro workflow. Nové hodnoty těchto polí budou přidány k dodavateli jako navržené změny a workflow se spustí automaticky.

4. Vyberte v seznamu polí dodavatele zaškrtávací políčko **Povolit** pro každé pole, které musí být schváleno před tím, než lze provést změny.
5. Přejděte do nabídky **Závazky \> Nastavení \> Workflow závazků**.
6. Vyberte možnost **Nový**.
7. Zvolte **Workflow navrhovaných změn dodavatele**. 
8. Nastavte workflow tak, aby odpovídalo vašemu procesu schvalování. Prvek schválení workflow **Schválení workflow pro navrhovanou změnu dodavatele** použije změny pro dodavatele.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Změna informace o dodavateli a odeslání změn do workflow

Při změně pole, které je povoleno pro workflow, se zobrazí stránka **Navrhované změny**. Tato stránka zobrazí původní hodnotu pole a novou hodnotu, kterou jste zadali. Pole, které jste změnili, se vrátí na původní hodnotu. Stavová zpráva také informuje o tom, že vaše změny nebyly odeslány. 

Vždy, když změníte pole, které je povoleno pro workflow, bude toto pole přidáno do seznamu na stránce **Navrhované změny**. Chcete-li zrušit navrženou hodnotu pro pole, použijte tlačítko **Zahodit** vedle pole v seznamu. Chcete-li zahodit všechny změny, použijte tlačítko **Zahodit všechny změny** v dolní části stránky. Vyberte **OK** a stránku zavřete.

Až budete mít alespoň jednu navrženou změnu, zobrazí se další dvě karty v podokně akcí: **Navržené změny** a **Workflow**.

1. Vyberte **Navržené změny**, otevře se stránka **Navržené změny** a zkontrolujte své změny.
2. Zvolte **Workflow \> Odeslat změny do workflow**.

    Stav na stránce se změní na **Změny čekající na schválení**.

Workflow postupuje podle standardního procesu workflow. Schvalovatel je přesměrován na stránku **Dodavatel**, kde může zkontrolovat změny na stránce **Navrhované změny** a poté zvolit **Workflow \> Schválit** pro schválení pracovního postupu. Po dokončení všech schválení jsou pole aktualizována hodnotami, které jste navrhli.
