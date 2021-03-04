---
title: Vytvoření nového produktu v Commerce
description: Toto téma popisuje, jak vytvořit nový produkt v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410741"
---
# <a name="create-a-new-product-in-commerce"></a>Vytvoření nového produktu v Commerce


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit nový produkt v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Produkt je definován především číslem, názvem a popisem. Jsou však požadována také další data za účelem popisu produktu nebo služby:

## <a name="create-a-new-product"></a>Vytvoření nového produktu

1. V navigačním podokně přejděte na **Moduly \> Retail and Commerce \> Produkty a kategorie \> Produkty dle kategorie**.
1. V podokně akcí zvolte **Nový**.
1. V rozevíracím seznamu **Typ produktu** vyberte **položku** nebo **službu**.
1. V rozevíracím seznamu **Podtyp produktu** vyberte možnost **Produkt** (pokud produkt nebude mít žádné varianty) nebo **Základní produkt** (pokud produkt bude mít varianty).
1. Do pole **Číslo produktu** zadejte číslo produktu, pokud ještě není předem vyplněno.
1. Do pole **Název produktu** zadejte název produktu.
1. V poli **Vyhledat název** zadejte název pro vyhledání.
1. V rozevíracím seznamu **Maloobchodní kategorie** vyberte příslušnou kategorii.
1. Je-li produkt sadou, vyberte **Ano** pro **Produktovou sadu**.
1. Je-li dílčím typem produktu základní produkt, nastavte **Skupinu dimenzí produktu** tak, aby zahrnovala podporované varianty. Mezi možnosti patří **Barva**, **Vylikost**, **Styl** a **Konfigurace**. V případě potřeby bude pravděpodobně nutné vytvořit další skupiny dimenzí produktu.
1. V rozevíracím seznamu **Techologie konfigurace** vyberte příslušnou možnost.
1. Vyberte **OK**.

Následující obrázek znázorňuje příklad přidaného produktu.

![Vytvoření produktu](media/create-new-product.png)

Po přidání produktu lze pro něj nastavit další data, například **Popis produktu**, **Skupiny variant**, **Skupiny dimenzí**, **Atributy produktu** a **Související produkty**.

Následující obrázek znázorňuje další podrobnosti o produktu.

![Podrobnosti produktu](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Vytvořit varianty produktů

Je-li dílčím typem produktu **Základní produkt**, bude nutné vytvořit specifické varianty. 

Při vytváření produktových variant postupujte takto.

1. V podokně akcí vyberte **Varianty produktu**.
1. Pokud byly v podokně akcí vybrány skupiny variant, vyberte možnost **Návrhy variant*.
1. Vyberte varianty, které chcete pro produkt podporovat.
1. Vyberte **Vytvořit**.

## <a name="release-a-product"></a>Uvolnění produktu

Při prodeji produktu musí být nejprve uvolněn právnické osobě.

1. Na stránce produkt vyberte možnost **Uvolnit produkty**.

    ![Uvolnit produkt](media/create-new-product-3.png)

1. Vyberte produkt k uvolnění a pak klikněte na tlačítko **Další**.

    ![Vyberte produkt k uvolnění](media/create-new-product-4.png)

1. Vyberte sadu variant produktu k uvolnění a pak klikněte na tlačítko **Další**.

    ![Vyberte varianty k uvolnění](media/create-new-product-5.png)

1. Vyberte právnickou osobu a poté vyberte možnost **Další**.

    ![Zvolte právnickou osobu](media/create-new-product-6.png)

1. Vyberte **Dokončit**.

    ![Dokončit uvolnění produktu](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Konfigurovat uvolněný produkt

Jakmile je produkt uvolněn, bude vyžadovat další konfiguraci, která zahrnuje přidání ceny k produktu.

1. V navigačním okně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Uvolněné produkty podle kategorie**.
1. Vyberte uzel kategorie produktu, který byl uvolněn, a pak vyberte produkt ze seznamu produktů.
1. V podokně akcí vyberte **Upravit**.
1. V části **Nákup** nakonfigurujte všechny požadované vlastnosti včetně **jednotek**, **ceny** a **množství**.
1. V podokně akcí vyberte možnost **Ověřit** a zajistěte, aby pro chybějící pole nebyly hlášeny žádné chyby.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad konfigurace pro uvolněný produkt.

![Konfigurovat uvolněný produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a>Další zdroje

[Vytvořit právnické osoby](channels-legal-entities.md)

[Vytvoření skupiny variant](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]