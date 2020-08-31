---
title: Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce
description: V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27e4f1c751ee865b0df536f3c1912cb1d8946032
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664995"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.

## <a name="overview"></a>Přehled

V řešení Dynamics 365 Commerce jsou všechny informace o produktech a transakcích sledovány v úložišti entit prostředí. Chcete-li zpřístupnit tato data jiným službám Dynamics 365, jako například analýze dat, business intelligence a personalizovaná doporučení, je nutné připojit prostředí k řešení Azure Data Lake Storage Gen 2 vlastněnému zákazníkem.

Protože Azure Data Lake Storage je nakonfigurováno v prostředí, jsou všechna potřebná data zrcadlena z úložiště entit a přitom jsou stále chráněna a pod kontrolou odběratele.

Pokud jsou v prostředí také povolena doporučení produktu nebo přizpůsobená doporučení, bude mít zásobník doporučení produktu přístup k vyhrazené složce v Azure Data Lake Storage, aby bylo možné načíst data odběratele a vypočítávat doporučení na jejich základě.

## <a name="prerequisites"></a>Předpoklady

Zákazníci musí mít Azure Data Lake Storage nakonfigurované v předplatném Azure, které vlastní. Toto téma nezahrnuje nákup předplatného Azure nebo nastavení účtu úložiště s podporou Azure Data Lake Storage.

Další informace o Azure Data Lake Storage naleznete v [oficiální dokumentaci Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Kroky konfigurace

V této části jsou popsány konfigurační kroky, které jsou nezbytné pro povolení Azure Data Lake Storage v prostředí ve vztahu k doporučením produktu.
Podrobnější přehled kroků potřebných k povolení Azure Data Lake Storage naleznete v tématu [Nastavení úložiště entit jako Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Povolení Azure Data Lake Storage v prostředí

1. Přihlaste se k portálu administrativního systému prostředí.
1. Vyhledejte **Systémové parametry** a přejděte na kartu **Datová připojení**. 
1. Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.
1. Nastavte možnost **Postupná aktualizace Data Lake** na **Ano**.
1. Dále zadejte následující požadované informace:
    1. **ID aplikace** // **Tajný klíč aplikace** // **Název DNS** - Je třeba se připojit ke KeyVault, kde je uložen tajný klíč Azure Data Lake Storage.
    1. **Název tajného klíče** - Název tajného klíče uloženého v KeyVault a použitého k ověření s Azure Data Lake Storage.
1. Uložte své změny v levém horním rohu stránky.

Následující obrázek znázorňuje příklad konfigurace Azure Data Lake Storage.

![Příklad konfigurace Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Test připojení Azure Data Lake Storage

1. Otestujte připojení ke KeyVault pomocí odkazu **Testovat Azure Key Vault**.
1. Otestujte připojení k Azure Data Lake Storage pomocí odkazu **Testovat úložiště Azure**.

> [!NOTE]
> Pokud se testy nezdaří, zkontrolujte správnost výše popsaných informací o KeyVault a potom to zkuste znovu.

Jakmile jsou testy připojení úspěšné, je nutné povolit automatickou aktualizaci úložiště entit.

Chcete-li povolit automatickou aktualizaci pro úložiště entit, postupujte následujícím způsobem.

1. Vyhledávejte v **úložišti entit**.
1. V seznamu vlevo přejděte na položku **RetailSales** a vyberte možnost **upravit**.
1. Zkontrolujte, zda **Automatická aktualizace povolena** je nastaveno na **Ano**, zvolte **Obnovit** a pak vyberte **Uložit**.

Následující obrázek znázorňuje příklad úložiště entit s povolenou automatickou aktualizací.

![Příklad úložiště entit s povolenou automatickou aktualizací](./media/exampleADLSConfig2.png)

Azure Data Lake Storage je nyní nakonfigurováno pro prostředí. 

Pokud jste to již nedokončili, postupujte podle kroků pro [povolení doporučení produktu a individuální nastavení](enable-product-recommendations.md) pro dané prostředí.

## <a name="additional-resources"></a>Další prostředky

[Zpřístupnit úložiště entit jako Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Přehled doporučení produktu](product-recommendations.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)
