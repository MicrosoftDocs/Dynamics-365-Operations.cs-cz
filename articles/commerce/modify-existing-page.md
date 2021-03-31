---
title: Úprava existující webové stránky
description: Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6afd19a01520813e54871f4849aeb18f4424173c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223040"
---
# <a name="modify-an-existing-site-page"></a>Úprava existující webové stránky


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Pokud je nutné upravit stránku, otevřete ji nejprve v editoru stránek. Přejděte na web, který obsahuje vaši stránku, a pak v seznamu stránek najděte požadovanou stránku. Nemůžete-li stránku najít, můžete použít funkci bohatého vyhledávání nástroje pro vytváření. Zadejte přesný název stránky nebo zadejte několik prvních písmen a potom hvězdičku (\*). Zobrazí se filtrovaný seznam stránek. Pomocí tohoto seznamu můžete vyhledat požadovanou stránku. Po nalezení správné stránky vyberte název stránky a otevřete tak stránku v editoru stránek.

> [!TIP]
> Je-li stránka viditelná v inspektoru stránky, můžete vybrat možnost **Upravit** a před otevřením stránky v editoru stránek ji zkontrolovat. Tímto způsobem lze zkontrolovat více stránek najednou.

Po otevření stránky v editoru stránek se ujistěte, že je rezervována vám. Panel příkazů v redakčním nástroji je dynamický, kontextový a stavový. Z toho vyplývá, že se zobrazí pouze akce, které lze aktuálně provádět na stránce. Není-li například stránka pro vás zarezervována, v panelu příkazů se nezobrazí tlačítka **Uložit** a **Dokončit úpravy**. Stav stránky se také zobrazuje na pravé straně okna.

Pokud stránka dosud není rezervována, vyberte **Upravit** na panelu příkazů. Panel příkazů se změní, aby odrážel nový stav stránky. Obdržíte také oznámení o tom, že pro vás byla stránka rezervována.

Chcete-li provést vlastní změny, proveďte následující kroky. Často použijete stromovou strukturu osnovy stránky vlevo k vyhledání a výběru modulu, který chcete změnit, a poté proveďte změny v podokně vlastnosti vpravo. 

Vaše změna však může někdy zahrnovat přidání nebo odebrání modelů nebo fragmentů. Chcete-li přidat fragment nebo modul, vyhledejte úsek, do něhož chcete přidat modul nebo fragment, pomocí stromu osnovy stránek, a pak vyberte tlačítko se třemi tečkami (**...**) pro tento úsek. Zobrazí se nabídka obsahující příkazy pro přidání modulu nebo fragmentu. Chcete-li odebrat modul nebo fragment, vyhledejte jej a vyberte ve stromu osnovy stránek, vyberte tlačítko se třemi tečkami a pak vyberte příkaz pro odstranění modulu nebo fragmentu.

> [!TIP]
> Můžete také zobrazit a upravit vlastnosti libovolného modulu, který je viditelný v náhledu vizuálního tvůrce stránek, výběrem volby přímo.

Po provedení změn a zobrazení náhledu jejich účinku byste měli stránku uložit zaškrtnutím políčka **Dokončit úpravy** na panelu příkazů. 

Chcete-li změny publikovat ihned, vyberte možnost **Publikovat** na panelu příkazů. Bude publikována poslední vrácená verze stránky, kterou jste upravili, a zpřístupní se tak externím uživatelům, kteří web zobrazí. 

## <a name="example-change-the-video-on-the-home-page"></a>Příklad: Změna videa na domovské stránce

Následující příklad ukazuje, jak upravit domovskou stránku změnou videa, které se zobrazí v modulu přehrávač videa.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Stránky**.
1. Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.
1. Na příkazovém řádku vyberte možnost **Upravit**.
1. V osnově stránky vyberte úsek **Hlavní**.
1. V úseku **Hlavní** rozbalte všechny moduly plovoucího obsahu.
1. Vyhledejte a vyberte modul přehrávače videa.
1. V podokně vlastnosti vpravo vyberte vlastnost **video**. Zobrazí se okno pro výběr zdroje.
1. V okně peo výběr zdroje vyberte dostupný zdroj videa nebo vyberte možnost **Odeslat nový zdroj** a odešlete nový zdroj videa.
1. Vyberte **OK**.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Poznámky** zadejte **Změněné video** a pak vyberte **OK.**
1. Chcete-li zobrazit náhled aktualizované stránky, vyberte volbu **Náhled**. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.

## <a name="additional-resources"></a>Další zdroje

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]