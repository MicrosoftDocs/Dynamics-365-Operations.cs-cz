---
title: Workflow odběratele
description: Toto téma obsahuje informace o workflow odběratele. Změníte specifická pole pro odběratele a poté odešlete tyto změny ke schválení pomocí workflow, než budou přidána k odběrateli.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175861"
---
# <a name="customer-workflow"></a>Workflow odběratele

[!include [banner](../includes/banner.md)]

Do verze 8.0.4 bylo přidáno workflow odběratele. Můžete změnit specifická pole pro odběratele a poté odeslat tyto změny ke schválení pomocí workflow, než budou přidána k odběrateli.

## <a name="set-up-the-customer-workflow"></a>Nastavení workflow odběratele

Než můžete použít funkci workflow odběratele, musíte ji povolit.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
2. Na kartě **Obecné** na pevné záložce **Schválení odběratele** nastavte možnost **Povolit schválení odběratele** na **Ano** pro povolení funkce.
3. V poli **Chování datových entit** zvolte chování, které mají datové entity použít při importu dat:

    - **Povolit změny bez schválení** – Entita může aktualizovat záznam odběratele bez jeho zpracování pomocí workflow.
    - **Zamítnout změny** – Změny záznamu odběratele nelze provést. Import se nezdaří pro pole, která jsou povolena pro workflow.
    - **Vytvořit návrhy změny** – Budou změněna všechna pole, kromě polí, která jsou povolena pro workflow. Nové hodnoty pro tato pole budou přidány k odběrateli jako navrhované změny a workflow se automaticky spustí.

4. V seznamu polí odběratele zvolte zaškrtávací políčko **Povolit** pro každé pole, které musí být schváleno předtím, než lze provést změny.
5. Přejděte do **Pohledávky \> Nastavení \> Workflow pohledávek**.
6. Zvolte **Nové**.
7. Zvolte **Workflow navrhované změny odběratele**. 
8. Nastavte workflow, aby odpovídalo vašemu schvalovacímu procesu. Prvek schválení workflow **Schválení workflow pro navrhovanou změnu odběratele** použije změny odběratele.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Změna informací odběratele a odeslání změn do workflow

Když změníte pole, které je povoleno pro workflow, zobrazí se stránka **Navrhované změny**. Tato stránka zobrazí původní hodnotu pole a novou hodnotu, kterou jste zadali. Pole, které jste změnili, se vrátí na svou původní hodnotu. Stavová zpráva na stránce vás informuje o tom, že změny nebyly odeslány.

Pokaždé, když změníte pole, které je povoleno pro workflow, přidá se toto pole k seznamu navržených změn. Chcete-li zahodit navrhovanou hodnotu pro pole, použijte tlačítko **Zahodit** vedle pole v seznamu. Chcete-li zahodit všechny změny, použijte tlačítko **Zahodit všechny změny** ve spodní části stránky. Zvolte **OK** pro zavření stránky.

Jakmile máte alespoň jednu navrhovanou změnu, zobrazí se další dvě nabídky v podokně akcí: **Navrhované změny** a **Workflow**.

1. Zvolte **Navrhované změny** pro otevření stránky **Navrhované změny** a zkontrolujte své změny.
2. Zvolte **Workflow \> Odeslat** pro odeslání změn do workflow.

    Stav na stránce se změní na **Změny čekající na schválení**.

Workflow postupuje podle standardního procesu workflow v aplikaci. Schvalovatel je přesměrován na stránku **Odběratel**, kde může zkontrolovat změny na stránce **Navrhované změny** a poté zvolit **Workflow \> Schválit** pro schválení workflow. Po dokončení všech schválení jsou pole aktualizována hodnotami, které jste navrhli.