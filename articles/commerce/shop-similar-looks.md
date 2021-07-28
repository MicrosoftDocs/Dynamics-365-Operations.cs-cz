---
title: Povolit doporučení typu „podobný vzhled“
description: Toto téma popisuje, jak povolit v doporučení typu „podobný vzhled“ v produktu Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/06/2020
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c350e6d6bfd4e699c55a4c0a57695b1b718b7167
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357755"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Povolení doporučení „nákupu podobného vzhledu“

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak povolit v doporučení typu „podobný vzhled“ v produktu Microsoft Dynamics 365 Commerce.

Doporučení typu "podobný vzhled" v produktu Dynamics 365 Commerce využívá sílu umělé inteligence a strojového učení (AI-ML) k poskytování doporučení pro vizuálně podobné produkty zákazníkům. Poskytnutím doporučení typu „podobný vzhled“ pro všechny maloobchodní kanály v obchodě mohou maloobchodníci zvýšit spokojenost zákazníků tím, že zákazníkům pomohou snadno najít to, co chtějí.

Funkce pro doporučení „podobný vzhled obchodu“ používá obrazy produktů zárodečných variant produktů k nalezení a doporučování vizuálně podobných produktů v katalogu produktů maloobchodníka. 

Doporučení typu „podobný vzhled“ jsou k dispozici jak v místě prodeje (POS), tak v prostředí elektronického obchodování.

### <a name="example-scenarios"></a>Ukázkové scénáře

- Zákazník si prohlédne černý pruhovaný svetr a obdrží doporučení pro podobný svetr v červené. Zákazník vybere doporučený produkt místo původně prohlíženého produktu a poté obdrží doporučení pro podobné produkty v červené. 
- Zákazník používá doporučení typu „podobný vzhled“, aby objevil vyhovující náušnice pro prsten, který má zákazník zájem koupit.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>V centrále Commerce povolte doporučení typu „podobný vzhled“

Doporučení produktů jsou podporována pouze u užovatelů Commerce, kteří migrovali své úložiště do služby Azure Data Lake Gen2.

### <a name="prerequisites"></a>Předpoklady

Než mohou maloobchodníci začít zákazníkům zobrazovat doporučení typu „podobný vzhled“, musí provést dva nezbytné kroky:

- [Povolit doporučení produktů](enable-product-recommendations.md) v centrále Commerce.
- Ověřit, zda mediální server podporuje volání HTTPS.

Aby mohl modul doporučení získat přístup k obrázkům produktů, musí maloobchodníci vygenerovat adresy URL produktů. Při generování adres URL produktů v centrále aplikace Commerce postupujte následovně.

1. Přejděte do části **Obrázky produktu**.
1. V podokně Akce vyberte možnost **Definovat šablonu média**.
1. V **Definovat šablonu média** podokně vlastností, pod **Mediální adresy URL**, vyberte **Vygenerujte adresy URL**.

> [!NOTE]
> Když povolíte funkci doporučení typu „podobný vzhled“, začne proces generování seznamů doporučení produktů. Tyto seznamy budou k dispozici a budou viditelné online a v POS terminálech do následujícího dne.

Chcete-li aktivovat funkci doporučení typu „podobný vzhled“ v centrále Commerce, postupujte takto.

1. Přejděte na **Správu funkcí**.
1. V seznamu dostupných funkcí vyhledejte a vyberte **Doporučení typu podobný vzhled**.
1. V pravém podokně vyberte **Povolit** k zapnutí služby.

Následující obrázek ukazuje funkci **Doporučení typu „podobný vzhled“** na stránce **Správa funkcí** v centrále Commerce.

![Funkce Doporučení typu „podobný vzhled“ na stránce Správa funkcí v centrále Commerce.](./media/enableshopsimilarlooks.png)

Po dokončení předchozích úkolů bude do terminálů POS automaticky přidán kontextový panel **Doporučení podobných výrobků**. Výběrem **Zobrazit více** uživatelé POS terminálů mohou být přesměrováni na vyhrazenou stránku „podobný vzhled“, kterou lze dále filtrovat.

> [!NOTE]
> Pokud vypnete funkci doporučení typu „podobný vzhled“, nebudou ovlivněny žádné jiné typy doporučení produktů. Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Přidejte na stránky s podrobnostmi o produktech tlačítko Podobný vzhled pomocí tvůrce webu Commerce

Poté, co v centrále Commerce obchodu povolíte funkci doporučení typu „podobný vzhled“, tvůrce webu Commerce umožní maloobchodníkům přidat **Podobný vzhled** na nákupní stránce na jakékoli stránce s podrobnostmi o produktu (PDP). Zákazník, který vybere toto tlačítko, se přesune na vyhrazenou stránku „podobný vzhled“, která zobrazí vizuálně podobné produkty. Tam může zákazník pomocí selektorů dále filtrovat produkty.

K přidání tlačítka **Podobný vzhled** na PDP pomocí tvůrce webu Commerce, postupujte následujícím způsobem.

1. Otevře existující stránku konfigurátoru webu, která obsahuje modul buy boxu.
1. V levém navigačním podokně vyberte modul buy boxu.
1. V pravém navigačním podokně vyberte **Povolit odkaz na stránku Podobný vzhled** zaškrtávací políčko.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte. Po publikování stránky bude PDP obsahovat tlačítko **Podobný vzhled**.

Následující obrázek ukazuje zaškrtávací políčko **Povolit odkaz na stránku Podobný vzhled** a tlačitko **Podobný vzhled** na příkladu PDP ve tvůrci webů.

![Zaškrtávací políčko Povolit odkaz na stránku Podobný vzhled a tlačitko Podobný vzhled na PDP ve tvůrci webů.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Přidat doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
