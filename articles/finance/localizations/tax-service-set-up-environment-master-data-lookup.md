---
title: Nastavení prostředí pro vyhledávání hlavních dat
description: Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4435dbfdb808a75b41a77d3c15d1c9fd29b266f353b1fbe18955ff985ab38bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718172"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Nastavení prostředí pro vyhledávání hlavních dat

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit prostředí tak, aby používalo funkci vyhledávání hlavních dat výpočtu daně.

1. Nastavte integraci power platform ve službě Lifecycle Services (LCS). Další informace naleznete v tématu [Integrace Microsoft Power Platform – Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Nastavte Dynamics 365 Finance a Microsoft Dataverse. Další informace viz [Získání řešení](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) a [Ověřování a autorizace](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Nastavte následující entity. Další informace viz [Povolení datových entit](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).
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
4. Nastavte Dynamics 365 Regulatory Configuration Service (RCS). 
5. Vytvořte požadavek na službu pro Microsoft, abyste povolili spuštění následujících funkcí:

      - Funkce ERCds
      - TaxServiceCDSFeature

6. V pracovním prostoru **Správa funkcí** a zapněte následující funkce:

      - (Preview) Podpora datových zdrojů Dataverse elektronického vykazování
      - (Preview) Podpora datových zdrojů Dataverse daňové služby
      - Globalizační funkce (Preview)

5. Přihlaste se k RCS pomocí účtu správce klienta.
6. Přejděte na **Elektronické vykazování** > **Připojené aplikace**. 
7. Vyberte **Nový** k přidání záznamu a zadejte následující informace do pole. 

   - Do pole **Název** zadejte název.
   - V poli **Typ** vyberte **Dataverse**.
   - Do pole **Aplikace** zadejte adresu URL Dataverse.
   - Do pole **Klient** zadejte klienta.
   - Do pole **Vlastní URL** zadejte svou adresu URL Dataverse a za ni napište „/api/data/v9.1“.

8. Vyberte **Zkontrolovat připojení** a dokončete proces připojení. 

   [![Tlačítko Zkontrolovat připojení.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Přejděte na **Elektronické výkaznictví** > **Daňové konfigurace** a importujte daňové konfigurace z [Daňové konfigurace](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Stránka Daňové konfigurace, strom datového modelu daní.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Přejděte na **Mapování modelu zdanitelného dokumentu** nebo **Mapování modelu Dataverse**, pokud používáte konfiguraci Microsoftu a v poli **Připojená aplikace** vyberte záznam, který jste vytvořili v kroku 7.
11. Nastavte možnost **Výchozí pro mapování modelu** na **Ano**.

   [![Stránka mapování modelu.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
