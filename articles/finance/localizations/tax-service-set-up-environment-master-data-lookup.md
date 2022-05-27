---
title: Povolit vyhledávání hlavních dat pro konfiguraci výpočtu daně
description: Toto téma vysvětluje, jak nastavit a aktivovat funkci vyhledávání hlavních dat pro výpočet daně.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7640144b1687fc64e55f659d49cdb0817c17294a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686704"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Povolit vyhledávání hlavních dat pro konfiguraci výpočtu daně 

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit a aktivovat funkci vyhledávání hlavních dat pro výpočet daně. K dispozici je rozevírací seznam pro výběr hodnot v konfiguraci výpočtu daně pro pole, například **Právnická osoba**, **Účet dodavatele**, **Kód položky** a **Termín doručení**. Tyto hodnoty pocházejí od připojeného prostředí Microsoft Dynamics 365 Finance s využitím zdroje dat Microsoft Dataverse.

> [!NOTE] 
> Funkce vyhledávání hlavních dat výpočtu daně je volitelná. Pokud deaktivujete funkci **Podpora zdrojů dat Dataverse daňové služby** ve službě Regulatory Configuration Service (RCS), můžete přeskočit následující kroky. V takovém případě však rozevírací seznam nebude dostupný v konfiguraci výpočtu daně.

1. Nastavte integraci Microsoft Power Platform ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace naleznete v tématu [Integrace Microsoft Power Platform – Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Po dokončení tohoto kroku se název prostředí Microsoft Power Platform objeví v části **Integrace Power Platform**.
2. Přejděte na [Centrum pro správu Microsoft Power Platform](https://admin.powerplatform.microsoft.com/environments) a vyberte název prostředí. Je zadána adresa URL prostředí.
3. Nastavte Dynamics 365 Finance a Dataverse. Další informace viz [Získání řešení virtuální entity](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) a [Ověřování a autorizace](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Nastavte následující entity. Další informace viz [Povolení virtuálních entit Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Nastavte Regulatory Configuration Service (RCS). Otevřete pracovní prostor **Správa funkcí** a zapněte následující funkce:

    - Podpora datových zdrojů Dataverse elektronického vykazování
    - Podpora datových zdrojů Dataverse daňové služby
    - Globalizační funkce

6. Přihlaste se k RCS pomocí účtu správce klienta.
7. Přejděte na **Elektronické vykazování** > **Připojené aplikace**. 
8. Vyberte **Nový** k přidání záznamu a zadejte následující informace do pole. 

    - Do pole **Název** zadejte název.
    - V poli **Typ** vyberte **Dataverse**.
    - Do pole **Aplikace** zadejte adresu URL Dataverse.
    - Do pole **Klient** zadejte klienta.
    - Do pole **Vlastní URL** zadejte svou adresu URL Dataverse a za ni napište „/api/data/v9.1“.

9. Vyberte **Zkontrolovat připojení** a dokončete proces připojení. 

    [![Tlačítko Zkontrolovat připojení.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Přejděte na **Elektronické výkaznictví** > **Daňové konfigurace** a importujte daňové konfigurace z [Daňové konfigurace](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Stránka Daňové konfigurace, strom datového modelu daní.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Přejděte na **Mapování modelu zdanitelného dokumentu** nebo **Mapování modelu Dataverse**, pokud používáte konfiguraci Microsoftu a v poli **Připojená aplikace** vyberte záznam, který jste vytvořili v kroku 7.
12. Nastavte možnost **Výchozí pro mapování modelu** na **Ano**.

    [![Stránka mapování modelu.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
