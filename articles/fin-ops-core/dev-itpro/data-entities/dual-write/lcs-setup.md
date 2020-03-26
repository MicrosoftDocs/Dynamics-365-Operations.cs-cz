---
title: Nastavení dvojitého zápisu z Lifecycle Services
description: V tomto tématu je vysvětleno, jak zřídit připojení s dvojím zápisem mezi novým prostředím Finance and Operations a novým prostředím Common Data Service z Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112403"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Nastavení dvojitého zápisu z Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V tomto tématu je vysvětleno, jak zřídit připojení s dvojím zápisem mezi novým prostředím Finance and Operations a novým prostředím Common Data Service z Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Předpoklady

Připojení s dvojím zápisem může nastavit pouze správce.

+ Musíte mít přístup k tomuto klientovi.
+ Musíte být správce v prostředích Finance and Operations i Common Data Service.

## <a name="set-up-a-dual-write-connection"></a>Nastavení připojení s dvojím zápisem

Chcete-li nastavit připojení s dvojím zápisem, postupujte následujícím způsobem.

1. V LCS přejděte na svůj projekt.
2. Pro nasazení nového prostředí vyberte **Konfigurace**.
3. Vyberte verzi. 
4. Vyberte topologii. Je-li k dispozici pouze jedna topologie, bude automaticky vybrána.
5. Proveďte první kroky v průvodci **Nastavení nasazení**.
6. Na kartě **Common Data Service** proveďte jeden z následujících kroků:

    - Pokud je prostředí Common Data Service již pro klienta zřízeno, můžete je vybrat.

        1. Nastavte možnost **Konfigurovat Common Data Service** na **Ano**.
        2. V poli **Dostupná prostředí** vyberte prostředí, které chcete integrovat s vašimi daty Finance and Operations. Seznam obsahuje všechna prostředí, v nichž máte oprávnění správce.
        3. Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.

        ![Karta Common Data Service, když už je pro klienta zřízeno prostředí Common Data Service](../dual-write/media/lcs_setup_1.png)

    - Pokud váš klient ještě nemá prostředí Common Data Service, bude zřízeno nové prostředí.

        1. Nastavte možnost **Konfigurovat Common Data Service** na **Ano**.
        2. Zadejte název prostředí Common Data Service.
        3. Vyberte oblast, ve které má být prostředí nasazeno.
        4. Vyberte výchozí jazyk a měnu pro prostředí.

            > [!NOTE]
            > Jazyk a měnu nelze později změnit.

        5. Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.

        ![Karta Common Data Service, pokud váš klient ještě nemá prostředí Common Data Service](../dual-write/media/lcs_setup_2.png)

7. Proveďte zbývající kroky v průvodci **Nastavení nasazení**.
8. Poté, co má prostředí stav **Nasazeno** otevřete stránku s podrobnostmi o prostředí. V sekci **Informace o prostředí Common Data Service** jsou uvedeny názvy prostředí Finance and Operations a Common Data Service, která jsou propojena.

    ![Sekce s informacemi o prostředí Common Data Service](../dual-write/media/lcs_setup_3.png)

9. Správce prostředí Finance and Operations se musí přihlásit k LCS a dokončit propojení výběrem **Odkaz na CDS for Apps**. Na stránce s podrobnostmi o prostředí jsou uvedeny kontaktní informace na správce.

    Po dokončení propojení se stav aktualizuje na **Propojení prostředí proběhlo úspěšně**.

10. Chcete-li otevřít pracovní prostor **Integrace dat** v prostředí Finance and Operations a ovládat šablony, které jsou k dispozici, vyberte možnost **Odkaz na CDS for Apps**.

    ![Tlačítko Odkaz na CDS for Apps v sekci s informacemi o prostředí Common Data Service](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Nelze zrušit propojení prostředí pomocí LCS. Chcete-li zrušit propojení prostředí, otevřete pracovní prostor **Integrace dat** v prostředí Finance and Operations a poté vyberte možnost **Zrušit propojení**.
