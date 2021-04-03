---
title: Zobrazení a export popisů polí
description: Tento článek popisuje, jak zobrazit popisy pole, a jak používat stránku Popisy pole pro export popisů.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265b540ba36b7526a8d6cb64f29157b6126e4dae
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566191"
---
# <a name="view-and-export-field-descriptions"></a>Zobrazení a export popisů polí

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak zobrazit popisy pole, a jak používat stránku Popisy pole pro export popisů.

Některá složitější pole mají popisy. Tyto popisy se zobrazí při přesunutí ukazatele myši na pole. Stránka **Popis polí** slouží také k zobrazení a exportu popisů polí.

Ne všechny stránky obsahují popis polí. Chceme poskytnout popisy pro složitější pole a nikoliv pro ty, kde je jejich použití zřejmé. Proto některé stránky nemají žádné popisy pole, některé stránky mají několik popisů a některé složitější stránky, například mnoho stránek s parametry, mají mnoho popisů.

Pokud máte přístup k vývojovému prostředí, můžete přidat nový popis polí nebo stávající popisy přizpůsobit. Můžete například přidat informace specifické pro společnost do popisu pole. Další informace naleznete viz [Přizpůsobení popisů pole](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Zobrazení popisu pole v uživatelském rozhraní

Popis polí lze zobrazit umístěním ukazatele myši na pole. Pokud není k dispozici žádný popis, zobrazí se po přesunutí ukazatele myši na pole název pole.

> [!NOTE]
> V aplikaci Dynamics AX 7.0 (únor 2016) lze popis pole zobrazit pouze na stránce **Popisy pole**.

Následující obrázek znázorňuje popis pole, který se zobrazí při přesunutí ukazatele myši na pole **Uzamknout položky během inventury**.

[![Příklad popisu pole](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Pomocí stránky Popis pole můžete zobrazit a exportovat nápovědu pro pole

Stránka **Popis polí** slouží e zobrazení a exportu popisů polí. Současně můžete zobrazit popisy, které jsou k dispozici na jedné stránce.

### <a name="view-the-descriptions-for-a-page"></a>Zobrazení popisů pro stránku

Pro zobrazení popisů pro stránku postupujte následovně.

- Do pole **Vybrat stránku** zadejte název stránky. Můžete také klepnutím na šipku otevřít seznam všech stránek a stránku vyhledat nebo seznam filtrovat.

Můžete použít také název stránky, která se zobrazí v uživatelském rozhraní (například: **Odběratelé**), nebo název kódu (název stromu AOT), který zpřístupníte kliknutím pravým tlačítkem myši na stránku (například **CustTable**).

Informace o různých způsobech, jak filtrovat seznam stránek, naleznete v části "Hledání stránky" níže v tomto článku.

Pokud jste nastavili možnost **Zahrnout pole bez popisu** na **Ano**, všechna pole na stránce se zobrazí bez ohledu na to, zda mají popis pole.

### <a name="export-the-descriptions-for-a-page"></a>Export popisů pro stránku

Pro exportování popisů pro stránku postupujte následovně.

1. Vyberte stránku v poli **Vybrat stránku**.
2. Klikněte na tlačítko **Otevřít v Microsoft Office** v pravém horním rohu a potom klikněte na možnost **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Hledání stránky

Vyhledat stránku v poli **Vybrat stránku** lze několika způsoby. V mnoha případech je nutné kliknout na tlačítko se šipkou v poli **Vybrat stránku** pro otevření rozevíracího seznamu a výběr z filtrovaného seznamu stránek.

- Zadejte část názvu a pak otevřete rozevírací seznam pro výběr z filtrovaného seznamu stránek.
- Otevřete rozevírací seznam a klikněte na záhlaví **Název stránky** v horní části seznamu, nebo na záhlaví **Název AOT stránky**. Otevře se dialogové okno, ve kterém můžete vybrat možnosti rozšířeného filtrování, jako například **Název stránky začíná na**.
- Zadejte úplný název stránky. Při použití této možnosti je nejvhodnější otevřít rozevírací seznam a zjistit, co další se nachází v seznamu, i když se zobrazí popis polí.

    - Pokud existuje jediná přesná shoda s názvem, tyto popisy polí se zobrazí na této stránce.
    - Pokud existuje více než jediná přesná shoda, nezobrazí se žádné popisy. Bude nutné otevřít rozevírací seznam a vybrat požadovanou možnost.
    - Pokud název, který jste zadali, je také částí názvu další stránky, zobrazí se popisy pro vaši stránku. Pokud ale otevřete rozevírací seznam, zobrazí se další stránky, které obsahují tento název.

Například nejsou zobrazeny žádné popisy, když zadáte **Inventura** do pole **Vybrat stránku**. Pokud kliknete na rozevírací seznam, zjistíte, že existují dvě stránky s názvem **Inventura** a také několik stránek, které obsahují v názvu slovo „Inventura“. Pokud vyberete stránku, který má název stromu AOT **InventJournalCount**, zobrazí se pro tuto stránku popisy polí. Pokud však znovu otevřete na rozevírací seznam, zobrazený seznam nyní obsahuje všechny stránky, které mají „InventJournalCount“ jako součást jejich názvu stromu AOT.

## <a name="troubleshooting"></a>Řešení potíží

Tato sekce obsahuje informace o řešení problémů, ke kterým může dojít při používání popisů pole.

### <a name="i-cant-find-a-field-description"></a>Nelze najít popis pole

Právě probíhá přidávání popisů pro složitější pole. Potřebujete-li nápovědu pro konkrétní pole, informujte nás přidáním komentáře k tomuto tématu.

### <a name="the-field-description-isnt-helpful"></a>Pole popisu není užitečné

Informujte nás přidáním komentáře k tomuto tématu. Pokud je to možné, uveďte další informace, které požadujete.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Nelze najít pole na stránce Popisy pole

Pokud chcete zobrazit všechna pole na stránce, nastavte pro možnost **Zahrnout pole bez popisu** hodnotu **Ano**. Klepněte na pole **Vybrat stránku** a ověřte, že jste vybrali správnou stránku. Pokud název, který jste zadali, je součástí názvu jiného pole, pravděpodobně jste vybrali stránku, který má delší název.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Nelze najít stránku na stránce Popisy pole

Informace o různých způsobech, jak vyhledat stránky, naleznete v části "Hledání stránek" dříve v tomto článku. Pokud jste zadali přesný název stránky, pravděpodobně nebudou zobrazeny v popisech polí, pokud existuje více než jedna stránka se stejným názvem. Klikněte na šipku v poli **Vybrat stránku**, abyste otevřeli filtrovaný seznam dostupných stránek.

## <a name="additional-resources"></a>Další zdroje

[Přizpůsobení popisů pole](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]