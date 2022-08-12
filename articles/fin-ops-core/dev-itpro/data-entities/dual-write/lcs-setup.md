---
title: Nastavení duálního zápisu z Lifecycle Services
description: Tento článek vysvětluje, jak nastavit připojení pro duální zápis z Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a002bae22044ea10be30340a87a191305f6c6b92
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111963"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Nastavení duálního zápisu z Lifecycle Services

[!include [banner](../../includes/banner.md)]



Tento článek vysvětluje, jak povolit duální zápis z Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Předpoklady

Zákazníci musejí vyplnit integraci Power Platform, jak je popsáno v následujících tématech:

- Pokud ještě nepoužíváte Microsoft Power Platform a chcete rozšířit své prostředí finančních a provozních aplikací přidáním možností platformy, přečtěte si téma [Integrace Power Platform – Aktivace po nasazení prostředí](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Pokud již máte prostředí Dataverse a Power Platform a chcete je propojit s prostředím finančních a provozních aplikací, viz [Integrace Power Platform – Aktivace po nasazení prostředí](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Nastavení duálního zápisu pro nová nebo existující prostředí Dataverse

Podle těchto pokynů nastavíte duální zápis ze stránky LCS **Podrobnosti o prostředí**:

1. Na stránce **Podrobnosti o prostředí** rozbalte sekci **Integrace Power Platform**.

2. Vyberte tlačítko **Aplikace pro dvojí zápis**.

    ![Integrace Power Platform.](media/powerplat_integration_step2.png)

3. Zkontrolujte smluvní podmínky a poté vyberte **Konfigurovat**.

4. Pokračujte volbou tlačítka **OK**.

5. Pokrok můžete sledovat pravidelným obnovováním stránky s podrobnostmi o prostředí. Nastavení obvykle trvá 30 minut nebo méně.  

6. Po dokončení nastavení vás bude informovat zpráva, zda byl proces úspěšný nebo zda došlo k selhání. Pokud se nastavení nezdařilo, zobrazí se související chybová zpráva. Před přechodem k dalšímu kroku musíte opravit všechny chyby.

7. Vyberte **Odkaz na prostředí Power Platform**, chcete-li vytvořit spojení mezi Dataverse a databázemi aktuálního prostředí. To obvykle trvá méně než 5 minut.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Odkaz na prostředí Power Platform.":::

8. Po dokončení propojení se zobrazí hypertextový odkaz. Pomocí odkazu se přihlaste do oblasti správy duálního zápisu v prostředí financí a provozu. Odtud můžete nastavit mapování entit.

## <a name="linking-mismatch"></a>Nesoulad propojení

Je možné, že vaše prostředí s duálním zápisem je propojeno s instancí Dataverse, zatímco služba LCS nemá nastavenu integraci Power Platform. Tento nesoulad propojení může způsobit neočekávané chování. Doporučuje se, aby se detaily prostředí LCS shodovaly s tím, k čemu jste připojeni v duálním zápisu, aby stejné připojení mohly používat obchodní události, virtuální tabulky a doplňky.

Pokud ve vašem prostředí existuje nesoulad propojení, LCS zobrazí na stránce s podrobnostmi o vašem prostředí varování podobající se následujícímu příkladu: „Microsoft zjistil, že je vaše prostředí propojeno pomocí duálního zápisu do jiného cíle, než je uvedeno v integraci Power Platform, což se nedoporučuje“:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integrace - neshoda propojení":::

Pokud se zobrazí toto varování, zkuste jedno z následujících řešení:

- Pokud vaše prostředí LCS nemělo nikdy nastavenu integraci Power Platform, můžete se připojit k instanci Dataverse, která je konfigurována pro duální zápis podle pokynů v tomto článku.
- Pokud vaše prostředí LCS již má nastavenu integraci Power Platform, měli byste zrušit propojení duálního zápisu a znovu se připojit k cíli určenému LCS pomocí návodu v článku [Scénář: Obnova nebo změna propojení](relink-environments.md#scenario-reset-or-change-linking).

V minulosti byla k dispozici možnost ručního lístku podpory, ale to bylo předtím, než existovala možnost 1 výše.  Společnost Microsoft již nepodporuje požadavky na ruční opětovné propojení prostřednictvím lístků podpory.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

