---
title: Nastavení duálního zápisu z Lifecycle Services
description: Toto téma vysvětluje, jak nastavit připojení pro duální zápis z Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 9f461837c65c30eace3358c231618aedf428f487
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675290"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Nastavení duálního zápisu z Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma vysvětluje, jak povolit duální zápis z Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Předpoklady

Musíte vyplnit integraci Power Platform, jak je popsáno v následujících tématech:

+ [Integrace Power Platform - povolit během nasazení prostředí](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Integrace Power Platform – povolit po nasazení prostředí](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Nastavení duálního zápisu pro nová prostředí Dataverse

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

8. Po dokončení propojení se zobrazí hypertextový odkaz. Pomocí odkazu se přihlaste do oblasti správy duálního zápisu v prostředí Finance and Operations. Odtud můžete nastavit mapování entit.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Nastavení duálního zápisu pro existující prostředí Dataverse

Chcete-li nastavit duální zápis pro existující prostředí Dataverse, musíte vytvořit [lístek podpory](../../lifecycle-services/lcs-support.md) společnosti Microsoft. Lístek musí obsahovat:

+ ID vašeho prostředí Finance and Operations.
+ Název vašeho prostředí ze služby Lifecycle Services.
+ ID organizace Dataverse nebo ID prostředí Power Platform z Centra pro správu Power Platform. Ve svém lístku požádejte, aby ID bylo použito jako instance integrace Power Platform.

> [!NOTE]
> Nelze zrušit propojení prostředí pomocí LCS. Chcete-li zrušit propojení prostředí, otevřete pracovní prostor **Integrace dat** v prostředí Finance and Operations a poté vyberte možnost **Zrušit propojení**.

## <a name="linking-mismatch"></a>Nesoulad propojení

Je možné, že vaše prostředí LCS je propojeno s jednou instancí Dataverse, zatímco vaše prostředí duálního zápisu je propojeno s jinou instancí Dataverse. Tento nesoulad propojení může způsobit neočekávané chování a může dojít k odeslání dat do nesprávného prostředí. Doporučené prostředí pro duální zápis je prostředí, které je vytvořeno jako součást integrace Power Platform a dlouhodobě to bude jediný způsob, jak vytvořit propojení mezi prostředími.

Pokud má vaše prostředí nesoulad propojení, LCS zobrazí na stránce s podrobnostmi o vašem prostředí varování „Microsoft zjistil, že je vaše prostředí propojeno pomocí duálního zápisu do jiného cíle, než je uvedeno v integraci Power Platform, což se nedoporučuje“:

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform integrace - neshoda propojení":::

Pokud narazíte na tuto chybu, existují dvě možnosti podle vašich potřeb:

+ [Odpojit a znovu propojit prostředí duálního zápisu (obnovit nebo změnit propojení)](relink-environments.md#scenario-reset-or-change-linking), jak je uvedeno na stránce podrobností o vašem prostředí LCS. Toto je ideální volba, protože ji můžete spustit bez podpory společnosti Microsoft.  
+ Pokud chcete zachovat své propojení v duálním zápisu, můžete požádat o pomoc podporu společnosti Microsoft a změnit integraci Power Platform, abyste využili své stávající prostředí Dataverse, jak je dokumentováno v předchozí části.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
