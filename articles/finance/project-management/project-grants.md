---
title: Granty projektu
description: Toto téma vysvětluje postup při vytváření a úpravě grantu.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282816"
---
# <a name="project-grants"></a>Granty projektu

[!include [banner](../includes/banner.md)]

Grant je peněžní dar pro konkrétní účel nebo projekt. Obvykle existují omezení, jak lze peníze z grantu vynaložit. V části Řízení projektů a účetnictví můžete zadat a sledovat granty a definovat jejich vztahy k projektům a smlouvám projektů. Můžete například provést následující úlohy:

- Přiřaďte granty k projektům a zdrojům financování prostřednictvím odkazů na stránky **Projekt** a **Podrobnosti o projektové smlouvě**.
- Zadávejte a sledujte změny grantu, jak přechází z jednoho stavu do druhého.
- Zadání a sledování nákladů, požadovaných částek a přiznaných částek.
- Vytvořte předlohu grantů a přidružte dílčí granty k ní.

Grant můžete vytvořit zadáním všech podrobností do nového záznamu, nebo můžete zkopírovat a aktualizovat podrobnosti o existujícím grantu.

## <a name="create-a-new-grant"></a>Vytvořit nový grant

1. Přejděte na **Řízení a účetnictví projektů** \> **Granty** \> **Granty**.
2. Vyberte **Nový** \> **Grant**.
3. Na stránce Podrobnosti o grantu na pevné záložce **Obecné** zadejte do pole **ID grantu** alfanumerický identifikátor pro grant.
4. Do pole **Název grantu** zadejte jedinečný název grantu.
5. Do pole **Popis** přidejte podrobnosti o novém grantu.

    Většina ostatních polí na stránce je volitelná a můžete zadat libovolné množství informací.

    V následujícím seznamu jsou uvedeny informace, které jsou zadány na jednotlivých pevných záložkách na stránce Podrobnosti o grantu:

    - **Obecné** - Zadejte podrobnosti o názvu, stavu, popisu, účelu a částce grantu.
    - **Kontaktní informace** – Zadejte podrobnosti o pracovnících a odděleních, kteří se budou starat o grant, a o zákazníkovi grantu nebo organizaci, která je zdrojem grantu. Můžete také zadat, zda je organizace předávací entitou, která obdrží grant a předá jej jinému příjemci. Klikněte na položku **Přidat** a přidejte kontaktní údaje, jako jsou telefonní čísla a e-mailové adresy, organizace, která poskytuje grant.
    - **Data a termíny** – Zadejte data, která se týkají grantu a jeho použití. Jedná se například o termín přihlášky, datum odeslání a datum schválení nebo zamítnutí grantu.
    - **Přidružené projekty a projektové smlouvy** – informace na této pevné záložce lze zadat pouze v případě, že pole **Stav** na pevné záložce **Obecné**  je nastavené na **Aktivní** nebo **Přiděleno**. Chcete-li dokončit související úkol, vyberte některou z následujících možností:

        - **Přidat zdroj financování** – Přidat nový zdroj financování pro grant. Můžete zadat všechny podrobnosti nyní, nebo použijte výchozí informace a aktualizujte je později.
        - **Přidat projektovou smlouvu** – přidat nebo aktualizovat informace o smlouvě projektu.
        - **Přidat projekt** – Přidat nebo aktualizovat podrobnosti projektu.

    - **Nastavení** – zadejte podrobnosti o odpovídajících finančních prostředcích, pokud jsou tyto informace požadovány. Mnoho organizací, které granty udělují, vyžaduje, aby příjemci utratili určitou částku z vlastních peněz nebo prostředků tak, aby odpovídala částce, která je poskytnuta v rámci grantu. V poli **Místní projekt nebo ID sledování** můžete zadat identifikátor, který se liší od identifikátoru projektu.

        > [!NOTE]
        > Pokud bude část grantu udělena jiné organizaci, nastavte možnost **Subgrantor** option to **Ano**. Pro granty, které se udělují v USA, můžete určit, zda grant bude udělen v rámci státu nebo federální pravomoci.

    - **Podrobnosti o čerpáni** – Přidat nebo aktualizovat informace o tom, jak často mohou být finanční prostředky vybírány, fakturovány nebo utráceny.

## <a name="create-a-new-grant-from-a-copy"></a>Vytvořit nový grant z kopie

1. Přejděte na **Řízení a účetnictví projektů** \> **Granty** \> **Granty**.
2. Vyberte **Nový** \> **Kopie z grantu**.
3. Zadejte alfanumerický identifikátor a název pro nový grant a potom vyberte tlačítko **OK**.
4. Na stránce Podrobnosti o grantu zkontrolujte podrobnosti zkopírovaného grantu a proveďte požadované změny. Většina polí na stránce je volitelná.

## <a name="view-or-modify-grant-details"></a>Zobrazit nebo upravit podrobnosti o grantu

1. Přejděte na **Řízení a účetnictví projektů** \> **Granty** \> **Granty**.
2. Vyberte drant, který chcete upravit.
3. V podokně akcí na kartě **Grant** ve skupině **Spravovat** zvolte **Uptavit**.
4. Zkontrolujte podrobnosti o grantu a proveďte požadované změny.
