---
title: Vytvoření šablony procesu náboru v aplikaci Attract
description: Toto téma poskytuje informace o způsobu vytvoření šablony procesu náboru v aplikaci Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460610"
---
# <a name="create-a-hiring-process-template-in-attract"></a>Vytvoření šablony procesu náboru v aplikaci Attract

[!include [banner](includes/banner.md)]

*Šablona náborového procesu* obsahuje všechny aktivity, které mají být zahrnuty jako součást náborového procesu pro práci. Toto téma popisuje prvky šablony procesu v aplikaci Microsoft Dynamics 365 Talent: Attract. Také vysvětluje, jakým způsobem vytvořit šablonu.

> [!NOTE]
> Vytvoření šablony je součástí doplňku komplexního náboru pro Attract.

## <a name="template-management"></a>Správa šablony

Organizace mohou rozhodnout, zda členové týmu nebo pouze správci mohou v aplikaci Attract vytvářet šablony procesů. Chcete-li nakonfigurovat správu šablon, přejděte na **Centrum pro správu** \> **Správa šablony**. Chcete-li nechat členy týmu vytvořit své vlastní šablony, zapněte správu šablony. Pokud správu šablony nezapnete, mohou šablony vytvářet pouze správci šablony.

## <a name="default-template"></a>Výchozí šablona

Pouze správci mohou nastavit výchozí šablonu. Výchozí šablona se používá tehdy, když není při vytváření práce vybrána šablona. Chcete-li nastavit výchozí šablonu, přejděte na **Centrum pro správu** \> **Správa šablony**. Na kartě šablony, která má být výchozí šablonou, vyberte tlačítko se třemi tečkami (**...**) a poté vyberte **Nastavit jako výchozí**.

## <a name="create-a-process-template"></a>Vytvoření šablony procesu

Správci, náboroví pracovníci a náboroví manažeři mohou vytvářet šablony procesu. Šablona procesu se skládá z *fází* a *aktivit*. Fáze seskupují dohromady jednu nebo více aktivit. Ve výchozím nastavení má každá šablona procesu aktivity Potenciální uchazeč, Žádost a Nabídka. Fáze, které obsahují tyto činnosti, lze přejmenovat. Můžete přidat další fáze výběrem **+ Nová fáze**. Aktivity můžete přidávat do fáze buď jejich přetažením do příslušné fáze, nebo dvojitým kliknutím na aktivitu v seznamu aktivit.

> [!NOTE]
> Názvy fází jsou viditelné pro kandidáty na stránce **Stav přihlášky**. Tuto skutečnost je třeba zvážit při výběru názvů fází.

Další informace o aktivitách naleznete v tématu [Aktivity procesu náboru](./activities-attract.md).

Pro vytvoření šablony náborového procesu postupujte podle těchto kroků:

1. Přejděte na **Šablony**.
2. Zvolte **Nové**.
3. V poli **Název šablony** zadejte název šablony a pak vyberte **Vytvořit**.
4. V seznamu **Zvolit schvalovací proces** vyberte **Výchozí**, aby práce vyžadovala schválení.
5. Výběrem povolte nebo zakažte potenciální uchazeče.
6. Volitelné: Přidejte nebo odeberte fáze.

    - Chcete-li přidat fázi, vyberte **+ nová fáze**.
    - Chcete-li odebrat fázi, najeďte myší nad fázi a poté zvolte tlačítko koše, které se objeví.

        > [!NOTE]
        > Fáze Potenciální uchazeč, Žádost a Nabídka nemohou být odstraněny, ale lze je přejmenovat.

7. Volitelné: Přidejte nebo odeberte aktivity.

    - Pokud chcete přidat aktivitu, přetáhněte ji ze seznamu aktivit na pravé straně do příslušné fáze. Případně na aktivitu dvakrát klikněte a pak vyberte fázi, do které ji chcete přidat.
    - Chcete-li odstranit aktivitu, rozbalte jí a pak vyberte tlačítko koše na záhlaví aktivity.

8. Zvolte **Uložit**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]