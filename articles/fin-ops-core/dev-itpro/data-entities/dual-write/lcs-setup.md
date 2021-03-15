---
title: Nastavení duálního zápisu z Lifecycle Services
description: Toto téma vysvětluje, jak nastavit připojení pro duální zápis z Microsoft Dynamics Lifecycle Services (LCS).
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: df67e498b963af3ded7464f46f37bb4b2ca7d852
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127586"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Nastavení duálního zápisu z Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

V tomto tématu je vysvětleno, jak zřídit připojení s dvojím zápisem mezi novým prostředím Finance and Operations a novým prostředím Dataverse z Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Předpoklady

Připojení s dvojím zápisem může nastavit pouze správce.

+ Musíte mít přístup k tomuto klientovi.
+ Musíte být správce v prostředích Finance and Operations i Dataverse.

## <a name="set-up-a-dual-write-connection"></a>Nastavení připojení s dvojím zápisem

Chcete-li nastavit připojení s dvojím zápisem, postupujte následujícím způsobem.

1. V LCS přejděte na svůj projekt.
2. Pro nasazení nového prostředí vyberte **Konfigurace**.
3. Vyberte verzi. 
4. Vyberte topologii. Je-li k dispozici pouze jedna topologie, bude automaticky vybrána.
5. Proveďte první kroky v průvodci **Nastavení nasazení**.
6. Na kartě **Dataverse** proveďte jeden z následujících kroků:

    - Pokud je prostředí Dataverse již pro klienta zřízeno, můžete je vybrat.

        1. Nastavte možnost **Konfigurovat Dataverse** na **Ano**.
        2. Ve sloupci **Dostupná prostředí** vyberte prostředí, které chcete integrovat s vašimi daty Finance and Operations. Seznam obsahuje všechna prostředí, v nichž máte oprávnění správce.
        3. Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.

        ![Karta Dataverse, když už je pro klienta zřízeno prostředí Dataverse](../dual-write/media/lcs_setup_1.png)

    - Pokud váš klient ještě nemá prostředí Dataverse, bude zřízeno nové prostředí.

        1. Nastavte možnost **Konfigurovat Dataverse** na **Ano**.
        2. Zadejte název prostředí Dataverse.
        3. Vyberte oblast, ve které má být prostředí nasazeno.
        4. Vyberte výchozí jazyk a měnu pro prostředí.

            > [!NOTE]
            > Jazyk a měnu nelze později změnit.

        5. Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.

        ![Karta Dataverse, pokud váš klient ještě nemá prostředí Dataverse](../dual-write/media/lcs_setup_2.png)

7. Proveďte zbývající kroky v průvodci **Nastavení nasazení**.
8. Poté, co má prostředí stav **Nasazeno** otevřete stránku s podrobnostmi o prostředí. V sekci **Integrace prostředí Power Platform** jsou uvedeny názvy prostředí Finance and Operations a Dataverse, která jsou propojena.

    ![Sekce integrace Power Platform](../dual-write/media/lcs_setup_3.png)

9. Správce prostředí Finance and Operations se musí přihlásit k LCS a dokončit propojení výběrem **Odkaz na CDS for Apps**. Na stránce s podrobnostmi o prostředí jsou uvedeny kontaktní informace na správce.

    Po dokončení propojení se stav aktualizuje na **Propojení prostředí proběhlo úspěšně**.

10. Chcete-li otevřít pracovní prostor **Integrace dat** v prostředí Finance and Operations a ovládat šablony, které jsou k dispozici, vyberte možnost **Odkaz na CDS for Apps**.

    ![Tlačítko Odkaz na CDS for Apps v sekci s informacemi o Power Platform](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Nelze zrušit propojení prostředí pomocí LCS. Chcete-li zrušit propojení prostředí, otevřete pracovní prostor **Integrace dat** v prostředí Finance and Operations a poté vyberte možnost **Zrušit propojení**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]