---
title: Povolení ADLS v prostředí Dynamics 365 Commerce
description: V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage (ADLS) pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025230"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>Povolení ADLS v prostředí Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak povolit a testovat Azure Data Lake Storage (ADLS) pro prostředí Dynamics 365 Commerce, což je předpokladem pro povolení doporučení produktu.

## <a name="overview"></a>Přehled

V řešení Dynamics 365 Commerce jsou všechny informace o produktech a transakcích sledovány v úložišti entit prostředí. Chcete-li zpřístupnit tato data jiným službám Dynamics 365, jako například analýze dat, business intelligence a personalizovaná doporučení, je nutné připojit prostředí k řešení Azure Data Lake Storage Gen 2 (ADLS) vlastněnému zákazníkem.

Protože ADLS je nakonfigurováno v prostředí, jsou všechna potřebná data zrcadlena z úložiště entit a přitom jsou stále chráněna a pod kontrolou odběratele.

Pokud jsou v prostředí také povolena doporučení produktu nebo přizpůsobená doporučení, bude mít zásobník doporučení produktu přístup k vyhrazené složce v ADLS, aby bylo možné načíst data odběratele a vypočítávat doporučení na jejich základě.

## <a name="prerequisites"></a>Předpoklady

Zákazníci musí mít ADLS nakonfigurované v předplatném Azure, které vlastní. Toto téma nezahrnuje nákup předplatného Azure nebo nastavení účtu úložiště s podporou ADLS.

Další informace o ADLS naleznete v [oficiální dokumentaci ADLS](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Kroky konfigurace

V této části jsou popsány konfigurační kroky, které jsou nezbytné pro povolení ADLS v prostředí.

### <a name="enable-adls-in-the-environment"></a>Povolení ADLS v prostředí

1. Přihlaste se k portálu administrativního systému prostředí.
1. Vyhledejte **Systémové parametry** a přejděte na kartu **Datová připojení**. 
1. Nastavte možnost **Povolit integraci s Data Lake** na **Ano**.
1. Nastavte možnost **Postupná aktualizace Data Lake** na **Ano**.
1. Dále zadejte následující požadované informace:
    1. **ID aplikace** // **Tajný klíč aplikace** // **Název DNS** - Je třeba se připojit ke KeyVault, kde je uložen tajný klíč ADLS.
    1. **Název tajného klíče** - Název tajného klíče uloženého v KeyVault a použitého k ověření s ADLS.
1. Uložte své změny v levém horním rohu stránky.

Následující obrázek znázorňuje příklad konfigurace ADLS.

![Příklad konfigurace ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>Test ADLS připojení

1. Otestujte připojení ke KeyVault pomocí odkazu **Testovat Azure Key Vault**.
1. Otestujte připojení k ADLS pomocí odkazu **Testovat úložiště Azure**.

> [!NOTE]
> Pokud se testy nezdaří, zkontrolujte správnost výše popsaných informací o KeyVault a potom to zkuste znovu.

Jakmile jsou testy připojení úspěšné, je nutné povolit automatickou aktualizaci úložiště entit.

Chcete-li povolit automatickou aktualizaci pro úložiště entit, postupujte následujícím způsobem.

1. Vyhledávejte v **úložišti entit**.
1. V seznamu vlevo přejděte na položku **RetailSales** a vyberte možnost **upravit**.
1. Zkontrolujte, zda **Automatická aktualizace povolena** je nastaveno na **Ano**, zvolte **Obnovit** a pak vyberte **Uložit**.

Následující obrázek znázorňuje příklad úložiště entit s povolenou automatickou aktualizací.

![Příklad úložiště entit s povolenou automatickou aktualizací](./media/exampleADLSConfig2.png)

ADLS je nyní nakonfigurováno pro prostředí. 

Pokud jste to již nedokončili, postupujte podle kroků pro [povolení doporučení produktu a individuální nastavení](enable-product-recommendations.md) pro dané prostředí.

## <a name="additional-resources"></a>Další zdroje

[Přehled doporučení produktu](product-recommendations.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Přidání seznamů doporučení produktu na stránky](add-reco-list-to-page.md)

[Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


