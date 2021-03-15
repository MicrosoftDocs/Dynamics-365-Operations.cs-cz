---
title: Povolit předpovědi plateb od zákazníka (náhled)
description: Toto téma vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009411"
---
# <a name="enable-customer-payment-predictions-preview"></a>Povolit předpovědi plateb od zákazníka (náhled)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech. Funkci zapnete v pracovním prostoru **Správa funkcí** a zadejte nastavení konfigurace na stránce **Parametry finančních přehledů**. Toto téma také obsahuje informace, které vám mohou pomoci tuto funkci efektivně využívat.

> [!NOTE]
> Než dokončíte následující kroky, nezapomeňte provést nezbytné kroky v tématu [Konfigurace pro finanční přehledy](configure-for-fin-insites.md).

1. Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí. Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu. (Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Pokud vaše nasazení Microsoft Dynamics 365 Finance je nasazení Service Fabric, můžete tento krok přeskočit. Tým finančních přehledů už měl testování zapnout za vás. Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.

2. Zapněte funkci přehledy plateb zákazníků:

    1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
    2. Najděte funkci, která je pojmenována **Přehledy plateb zákazníků (náhled)**.
    3. Vyberte **Povolit**.

    Funkce Přehledy plateb zákazníků je nyní zapnutá a připravená ke konfiguraci.

3. Konfigurujte funkci přehledy plateb zákazníků:

    1. Přejděte na **Kredit a inkasa \> Nastavení \> Finanční přehledy \> Parametry finančních přehledů**.

        [![Stránka parametrů finančních přehledů před konfigurací funkce](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Na stránce **Parametry finančních přehledů** na kartě **Přehledy plateb zákazníků** vyberte odkaz **Zobrazit datová pole použitá v predikčním modelu** pro otevření stránky **Datová pole pro predikční model**. Zde si můžete prohlédnout výchozí seznam polí, která se používají k vytvoření modelu predikce umělé inteligence (AI) pro předpovědi plateb zákazníků.

        Chcete-li k vytvoření predikčního modelu použít výchozí seznam polí, zavřete stránku **Datová pole pro predikční model** a poté na stránce **Parametry finančních přehledů** nastavte možnost **Povolit funkci** na **Ano**.

    3. Zadejte období transakce "velmi pozdě" a definujte, co predikční kontejner **Velmi pozdě** znamená pro vaši obchodní činnost.

        U každé otevřené faktury systém předpovídá pravděpodobnost platby ve třech kontejnerech: **Včas**, **Pozdě** a **Velmi pozdě**.

        - **Včas** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny v den splatnosti transakce nebo před ním.
        - **Pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po datu splatnosti transakce, ale před začátkem „velmi pozdního“ období transakce.
        - **Velmi pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po začátku „velmi pozdního“ období transakce.

        > [!NOTE]
        > Pokud změníte „velmi pozdní“ období transakce a vyberete **Změnit pozdní prhovou hodnotu** po vytvoření predikčního modelu AI pro platby odběratelům, stávající predikční model se odstraní a vytvoří se nový model. Nový predikční model přesune transakce do období „velmi pozdě“ na základě nastavení, která byla zadána k jeho definování.

    4. Poté, co dokončíte definování období transakce „velmi pozdě“, vyberte **Vytvořte predikční model** k vytvoření predikčního modelu. Část **Predikční model** na stránce **Parametry finančních přehledů** zobrazuje stav predikčního modelu.

        > [!NOTE]
        > Kdykoli během vytváření predikčního modelu můžete vybrat **Obnovit vytváření modelu** a restartovat proces.

    Funkce byla nyní nakonfigurována a je připravena k použití.

Poté, co byla funkce zapnuta a nakonfigurována a model predikce byl vytvořen a funguje, část **Predikční model** stránky **Parametry finančních přehledů** ukazuje přesnost modelu, jak je znázorněno na následujícím obrázku.

[![Přesnost predikčního modelu na stránce parametrů finančních přehledů](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Podrobnosti uvolnění

Veřejný náhled finančních přehledů je k dispozici pro zkušební nasazení v USA, Evropě a Velké Británii. Microsoft postupně přidává podporu pro další regiony.

Funkce veřejného náhledu mohou a měly by být zapnuty pouze v prostředích sandbox vrstvy 2. Modely nastavení a AI vytvořené v prostředí sandboxu nelze migrovat do produkčního prostředí. Další informace viz [Doplňkové podmínky použití pro náhledy Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]