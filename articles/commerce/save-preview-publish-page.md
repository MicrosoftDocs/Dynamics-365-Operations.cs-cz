---
title: Uložení, náhled a publikování stránky
description: Toto téma popisuje, jak uložit, zobrazit náhled a publikovat stránku v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db4866b22060b764fdde3e4a44e99e969133c0a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410875"
---
# <a name="save-preview-and-publish-a-page"></a>Uložení, náhled a publikování stránky

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak uložit, zobrazit náhled a publikovat stránku v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="save-a-page"></a>Uložení stránky

Chcete-li stránku uložit, je nutné ji rezervovat pro sebe a otevřít v editoru stránek. Chcete-li stránku odhlásit, vyberte možnost **Upravit** na řádku příkazů. Po dokončení úprav stránky byste ji měli ihned uložit, aby bylo zaručeno, že jsou uloženy provedené změny.

Při uložení stránky se tyto změny zobrazí pouze pro vás. Operace uložení je určena především pro uložení změn, zatímco stránka ještě není připravena k vrácení se změnami. Po dokončení úprav stránky doporučujeme, abyste ji vrátili se změnami, aby byly změny viditelné i pro ostatní. V tomto okamžiku může být stránka také rezervována jinými uživateli, kteří je musí upravit.

## <a name="preview-a-page"></a>Náhled stránky

Vývojový nástroj nabízí dva druhy funkcí náhledu: vizuální tvůrce stránek, což je podokno náhledu WYSIWYG v editoru stránek a v samostatném okně náhledu.

Když používáte editor stránek, zobrazí se v prostředním podokně náhled WYSIWYG. Tento náhled je automaticky aktualizován při každém uložení stránky. Aktualizaci můžete také provést ručně výběrem možnosti **Aktualizovat** na panelu příkazů. Náhled vykreslí stránku stejně, jako ji uvidí uživatelé webu, ale pomocníky pro vytváření obsahu jsou vykresleni nad ní.

Po dokončení úprav stránky můžete zobrazit náhled a zobrazit informace o tom, co se odběratelé uvidí. Chcete-li zobrazit náhled stránky, vyberte v panelu příkazů možnost **Náhled**. Náhled se zobrazí v samostatném okně prohlížeče. Stránka v okně náhledu je vykreslována tak, jak ji uživatel webu uvidí. Můžete změnit velikost okna, abyste se ujistili, že odpovídající moduly jsou správně vykresleny ve všech portech zobrazení.

> [!NOTE]
> Pro náhled nepublikovaného obsahu jsou vyžadovány ověření a správná oprávnění. Pokud tedy sdílíte adresu URL náhledu s někým, musí mít tato osoba správná oprávnění pro přístup k obsahu.

## <a name="publish-a-page"></a>Publikování stránky

Jakmile je stránka připravena, následujícím krokem bude publikování, aby mohli externí uživatelé zobrazit obsah. Před publikováním stránky je nutné ji vrátit se změnami výběrem možnosti **dokončit úpravy** na panelu příkazů.

Stránky můžete publikovat a zrušit jejich publikování pomocí inspektoru stránky nebo editoru stránek. Kontrola stránky zobrazuje seznam stránek a umožňuje hromadné operace. Editor stránek lze použít k publikování nebo zrušení publikování pouze jedné stránky, která je v ní otevřena.

Chcete-li publikovat jednu nebo více stránek z kontroloru stránek, vyberte je, zkontrolujte, zda jsou vráceny se změnami, a pak vyberte **Publikovat** na panelu příkazů. Stránky se publikují a obdržíte oznámení o operaci ve vývojovém nástroji.

Chcete-li publikovat jednu stránku z editoru stránek, je postup podobný. Když je stránka otevřena v editoru stránek, ujistěte se, že byla vrácena se změnami, a poté v panelu příkazů vyberte **Publikovat**. Stránka se publikuje a obdržíte oznámení o operaci ve vývojovém nástroji.

Při publikování stránky se publikuje pouze obsah stránky. Vy i ostatní uživatelé mohou přejít na stránku a zobrazit ji pouze po přidružení adresy URL. Adresa URL musí být publikována samostatně.

> [!IMPORTANT]
> Před publikováním stránky je nutné, aby všechny obrázky nebo fragmenty, které odkazují na stránku, již byly publikovány.

## <a name="save-preview-and-publish-a-home-page"></a>Uložení, náhled a publikování domovské stránky

Chcete-li uložit, zobrazit náhled a publikovat domovskou stránku, postupujte podle následujících kroků.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Stránky**.
1. Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.
1. Vyberte možnost **Upravit**.
1. Změňte stránku podle potřeby.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Poznámky** zadejte poznámku ohledně změn, které jste provedli, a poté vyberte **OK**.
1. Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.

## <a name="publish-a-url"></a>Publikování adresy URL

Adresu URL publikujete takto.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Adresy URL**.
1. Vyhledejte a vyberte adresu URL, kterou chcete publikovat.
1. Na příkazovém řádku vyberte možnost **Publikovat**.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)
