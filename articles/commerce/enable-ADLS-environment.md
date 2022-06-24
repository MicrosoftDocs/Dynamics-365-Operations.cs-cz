---
title: Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce
description: Tento článek obsahuje pokyny pro připojení k řešení Azure Data Lake Storage Gen 2 a úložiště entit prostředí Dynamics 365 Commerce. Toto je požadovaný krok před povolením doporučení produktů.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e0c84dd6b173a111b70a8adb6036be946149f7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885164"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Tento článek obsahuje pokyny pro připojení k řešení Azure Data Lake Storage Gen 2 a úložiště entit prostředí Dynamics 365 Commerce. Toto je požadovaný krok před povolením doporučení produktů.

V řešení Dynamics 365 Commerce jsou data nezbytná k výpočtu doporučení, produktů a transakcí agregována v úložišti Entity prostředí. Chcete-li zpřístupnit tato data jiným službám Dynamics 365, jako například analýze dat, business intelligence a personalizovaná doporučení, je nutné připojit prostředí k řešení Azure Data Lake Storage Gen 2 vlastněnému zákazníkem.

Po dokončení výše uvedených kroků se všechna zákaznická data v úložišti entit prostředí automaticky zrcadlí do řešení Azure Data Lake Storage Gen 2 zákazníka. Když jsou funkce doporučení povoleny prostřednictvím pracovního prostoru správy funkcí v centrále Commerce, bude zásobníku doporučení udělen přístup ke stejnému řešení Azure Data Lake Storage Gen2.

Během celého procesu zůstávají data zákazníků chráněna a pod jejich kontrolou.

## <a name="prerequisites"></a>Předpoklady

Úložiště entit prostředí Dynamics 365 Commerce musí být připojeno k účtu Azure Data Lake Gen Storage Gen2 a doprovodným službám.

Další informace o Azure Data Lake Storage Gen2 a o tom, jak ho nastavit, naleznete v [oficiální dokumentaci Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Kroky konfigurace

V této části jsou popsány konfigurační kroky, které jsou nezbytné pro povolení Azure Data Lake Storage Gen2 v prostředí ve vztahu k doporučením produktu.
Podrobnější přehled kroků potřebných k povolení Azure Data Lake Storage Gen2 naleznete v tématu [Nastavení úložiště entit jako Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Povolení Azure Data Lake Storage v prostředí

1. Přihlaste se k portálu administrativního systému prostředí.
1. Vyhledejte **Systémové parametry** a přejděte na kartu **Datová připojení**. 
1. Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.
1. Dále zadejte následující požadované informace:
    1. **ID aplikace** // **Tajný klíč aplikace** // **Název DNS** - Je třeba se připojit ke KeyVault, kde je uložen tajný klíč Azure Data Lake Storage.
    1. **Název tajného klíče** - Název tajného klíče uloženého v KeyVault a použitého k ověření s Azure Data Lake Storage.
1. Uložte své změny v levém horním rohu stránky.

Následující obrázek znázorňuje příklad konfigurace Azure Data Lake Storage.

![Příklad konfigurace Azure Data Lake Storage.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Test připojení Azure Data Lake Storage

1. Otestujte připojení ke KeyVault pomocí odkazu **Testovat Azure Key Vault**.
1. Otestujte připojení k Azure Data Lake Storage pomocí odkazu **Testovat úložiště Azure**.

> [!NOTE]
> Pokud se některý z testů nezdaří, ověřte správnost všech výše popsaných informací o KeyVault a potom to zkuste znovu.

Jakmile jsou testy připojení úspěšné, je nutné povolit automatickou aktualizaci úložiště entit.

Chcete-li povolit automatickou aktualizaci pro úložiště entit, postupujte následujícím způsobem.

1. Vyhledávejte v **úložišti entit**.
1. V seznamu vlevo přejděte na položku **RetailSales** a vyberte možnost **upravit**.
1. Zkontrolujte, zda **Automatická aktualizace povolena** je nastaveno na **Ano**, zvolte **Obnovit** a pak vyberte **Uložit**.

Následující obrázek znázorňuje příklad úložiště entit s povolenou automatickou aktualizací.

![Příklad úložiště entit s povolenou automatickou aktualizací.](./media/exampleADLSConfig2.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
