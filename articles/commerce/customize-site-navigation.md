---
title: Přizpůsobení navigace na webu
description: V tomto tématu je popsán postup při vytvoření přizpůsobené online hierarchie navigace pro uspořádání produktů pro procházení na webu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410768"
---
# <a name="customize-site-navigation"></a>Přizpůsobení navigace na webu


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při vytvoření přizpůsobené online hierarchie navigace pro uspořádání produktů pro procházení na webu Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Online výkladní skříně obvykle zákazníkům umožňují vyhledat a procházet produkty pomocí procházení kategorií produktů. Takovou možnost obvykle poskytují karty v horní části stránky nebo navigační panel vlevo. V řešení Dynamics 365 Commerce můžete vytvářet a spravovat hierarchickou strukturu navigace mezi kategoriemi a produkty zahrnuté do různých kategorií.

## <a name="create-a-channel-navigation-hierarchy"></a>Vytvoření hierarchie navigace sítě

Chcete-li vytvořit hierarchii navigace kanálu, postupujte následovně.

1. Přijděte na **Retail and Commerce \> Produkty a kategorie \> Správa kategorií a produktů**.
1. Vyberte **Hierarchie kategorií** a pak vyberte **Nová**.
1. Pojmenujte hierarchii.

    > [!NOTE]
    > Nejvyšší vytvořená kategorie je uzel kořenové kategorie. Tato stránka nebude zobrazena na vašem webu. Chcete-li vytvořit hierarchii kategorií, v níž se na webu zobrazí jeden uzel nejvyšší úrovně, vytvořte a pojmenujte kategorii jako podřízenou položku kořenové kategorie.

1. Vyberte možnost **Nový uzel kategorie** a pojmenujte kategorii.
1. Pokračujte ve vytváření kategorií na stejné a podřízené úrovni podle potřeby.

Nyní můžete přiřadit produkty ke každé kategorii, kterou jste vytvořili pod kategorií nejvyšší úrovně.

## <a name="customize-the-order-of-categories"></a>Vlastní nastavení pořadí kategorií

Ve výchozím nastavení se kategorie, které definujete, zobrazí v abecedním pořadí na webu. Lze však také přizpůsobit pořadí zobrazení kategorií.

## <a name="assign-a-category-hierarchy-type"></a>Přiřazení typu hierarchie kategorií

1. Přijděte na **Retail and Commerce \> Produkty a kategorie \> Správa kategorií a produktů**.
1. Vyberte možnost **Hierarchie kategorií**.
1. V podokně akcí na kartě **Hierarchie kategorií** ve skupině **Nastavení** zvolte **Přidružit typ hierarchie**.
1. Zvolte **Nové**.
1. V poli **Typ hierarchie kategorií** vyberte možnost **Hierarchie navigace kanálů**.
1. V poli **Hierarchie kategorií** vyberte hierarchii navigace sítě, kterou jste vytvořili dříve.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Publikování nových nebo aktualizovaných hierarchií navigací

Chcete-li hierarchii navigace zpřístupnit v online výkladní skříni, postupujte podle následujících kroků.

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Ve stromu vlevo vyberte svůj online obchod.
1. Vyberte možnost **Publikovat aktualizace kanálů**.
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. V seznamu vyhledejte a vyberte **Úloha 1040**.
1. Vyberte **Spustit**.
1. Zopakujte kroky 5 a 6 pro úlohy 1070 a 1150.

## <a name="show-categories-on-your-site"></a>Zobrazení kategorií na vašem webu

Chcete-li zobrazit hierarchii kategorií v online výkladní skříni, je nutné přidat modul navigační nabídky do příslušného umístění v šabloně nebo fragmentu. Modul navigační nabídky pak zobrazí hierarchii navigace za předpokladu, že jste publikovali hierarchii navigace v kanálu, na který je vázán váš web.

> [!NOTE]
> Modul navigační nabídky, který je součástí knihovny modulů, umožňuje uživatelům přejít pouze ke kategoriím, které nemají podkategorie. Chcete-li, aby vaši zákazníci mohli přejít do kategorií s podkategoriemi, je nutné upravit modul navigační nabídky.

## <a name="add-custom-navigation-options"></a>Přidání vlastních možností navigace

V navigační nabídce můžete přidat možnosti navigace, které nejsou součástí hierarchie kategorií produktů. Na konci seznamu kategorií produktů můžete například přidat položku **Kontaktujte nás**, která odkazuje na stránku kontaktu, kterou jste vytvořili pro váš web.

Chcete-li do navigační nabídky přidat vlastní možnosti navigace, postupujte následujícím způsobem.

1. V šabloně nebo fragmentu, který chcete přizpůsobit, vyberte modul navigační nabídky.
1. Chcete-li vytvořit novou navigační položku systému správy obsahu (CMS), v podokně vlastností na kartě **Data** vyberte možnost **Přidat položku**.
1. Zadejte text a adresu URL odkazu.
1. Chcete-li přidat další vlastní možnosti navigace, opakujte kroky 2 a 3.
1. Po dokončení tlačítkem **Uložit** uložte šablonu nebo fragment a poté výběrem možnosti **Dokončit úpravy** ji vraťte se změnami.

## <a name="additional-resources"></a>Další prostředky

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)

[Práce s fragmenty](work-with-fragments.md)

[Práce s moduly](work-with-modules.md)

[Vytvoření URL adresy stránky](create-page-url.md)

[Práce se skupinami publikování](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]