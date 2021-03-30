---
title: Práce s moduly
description: V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210892"
---
# <a name="work-with-modules"></a>Práce s moduly

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Moduly jsou logické stavební bloky, které tvoří strukturu stránek a mají různé účely a zaměření. Některé moduly jsou kontejnery vysoké úrovně a jejich jediným účelem je obsahování a uspořádání dalších modulů (podřízených modulů). Ostatní moduly, jako je například jednoduchý modul umístění obrázku, mají velmi specifický účel. Mezi těmito dvěma kategoriemi patří i jiné moduly, například karuselový modul.

Ve výchozím nastavení váš web Dynamics 365 Commerce obsahuje knihovnu modulů, která umožňuje dosáhnout většiny základních scénářů e-Commerce. Pomocí pouze těchto modulů by mělo být možné vytvořit komplexní web e-Commerce. Můžete však také přizpůsobit tyto moduly nebo sestavit nové, vlastní moduly pro specifické potřeby. Chcete-li vytvořit vlastní moduly, je k dispozici sada SDK (Software Development Kit), která usnadňuje vytvoření vlastní knihovny modulů.

## <a name="container-modules-and-slots"></a>Moduly a sloty kontejneru

Jak bylo zmíněno dříve, některé moduly jsou navrženy pro uchovávání podřízených modulů. Tyto moduly jsou označovány jako *kontejnery* a umožňují hierarchie vnořených modulů. Kontejnerové moduly obsahují *sloty*. Sloty se používají k obsluze rozvržení a účelu podřízených modulů v kontejneru. Příkladem může být základní modul kontejneru stránky (modul nejvyšší úrovně pro libovolnou stránku), který definuje několik důležitých slotů:

- Slot záhlaví
- Slot dílčího záhlaví
- Hlavní slot
- Slot zápatí
- Slot dílčího zápatí

Vývojář modulu definuje tyto sloty a určuje, které podřízené moduly a kolik podřízených modulů je možné přímo do ní vložit. Například slot záhlaví může podporovat pouze jeden modul typu **Modulu záhlaví**, zatímco slot obsahu může podporovat neomezený počet modulů typu (kromě jiných modulů kontejneru stránky).

V nástrojích pro vytváření obsahu nemusí autoři stránek předem vědět, které moduly lze a nelze vložit do jednotlivých slotů. Když autoři stránek vybírají slot a pak se pokusí vybrat modul, který se má přidat, uvidí filtrované zobrazení typů modulů, které jsou pro daný slot podporovány.

## <a name="content-modules"></a>Moduly obsahu

Moduly obsahu obsahují obsah a multimediální prvky, například text (například nadpisy, odstavce a odkazy) nebo odkazy na materiály (například obrázky, video a PDF). Typické typy modulů obsahu zahrnují moduly obsahu, blok textu a propagační bannerové moduly. Moduly těchto tří typů mohou obsahovat text nebo média a nevyžadují žádné podřízené moduly, aby je bylo možné zobrazit na stránce.

Většina typických, každodenních aktivit vytváření stránek a obsahu zahrnuje moduly obsahu, především proto, že tyto moduly definují skutečný obsah, který je vykreslený v nadřazených modulech kontejnerů. K dispozici je mnoho modulů obsahu a tyto moduly jsou obvykle posledními částmi, které přidáte do hierarchie vnořených modulů.

Následující ilustrace znázorňuje, jak jsou moduly vnořené v nadřazených slotech modulu kontejneru.

![Vnoření modulů](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Přidat nebo odebrat moduly

Následující postupy popisují způsob přidávání a odebírání modulů.

### <a name="add-a-module"></a>Přidat modul

Chcete-li přidat modul do slotu nebo kontejneru na stránce, postupujte podle následujících kroků.

1. V podokně obrysu vlevo nebo přímo na hlavním plátně vyberte kontejner nebo slot, do kterých lze přidat podřízený modul.

    > [!NOTE]
    > Návrhář modulů definuje seznam typů modulů, které lze přidat do určitého slotu modulu. Autoři šablon pak mohou vylepšit povolené možnosti modulu, aby zajistily konzistentní optimalizaci vyhledávače (SEO) a efektivitu vytváření pro všechny stránky, které jsou vytvořeny z určité šablony. Při přidání modulu do slotu je automaticky filtrováno dialogové okno **Přidat modul**, takže zobrazuje pouze moduly, které jsou podporovány ve vybraném kontejneru nebo slotu. Tento seznam povolených modulů je určen šablonou stránky nebo definicí modulu kontejneru.

1. Pokud používáte podokno obrysu, vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu a poté vyberte **Přidat modul**. Pokud používáte ovládací prvky přímo na plátně, vyberte symbol plus (**+**) v prázdném slotu nebo v sousedství aktuálně vybraného modulu a poté vyberte **Přidat modul**.

    > [!NOTE]
    > Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat modul** k dispozici.

1. V dialogovém okně **Přidat modul** vyhledejte a vyberte modul, který chcete přidat na svoji stránku.

    > [!TIP]
    > **Blok obsahu** je dobrým typem modulu pro začátečníky.

1. Výběrem tlačítka **OK** přidáte vybraný modul do vybraného kontejneru nebo slotu na stránce.

### <a name="remove-a-module"></a>Odebrání modulu

Chcete-li odebrat modul ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.

1. V podokně obrysu vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu, který chcete odebrat, a pak vyberte symbol odpadkového koše. Alternativně můžete na hlavním plátně vybrat symbol koše na panelu nástrojů vybraného modulu.
1. Až budete vyzváni k potvrzení odebrání modulu, vyberte **OK.**

## <a name="move-a-module-to-a-new-position"></a>Přesunutí modulu na novou pozici

Chcete-li přesunout modul na nové místo na stránce, použijte některou z následujících metod.

### <a name="move-a-module-using-the-outline-pane"></a>Přesuňte modul pomocí podokna obrysu

Chcete-li přesunout modul pomocí podokna obrysu, postupujte takto.

1. Vyberte a podržte modul, který chcete přesunout, v podokně obrysu, a poté modul přetáhněte na nové místo v obrysu. Modrá čára v obrysu a na plátně označuje, kam lze modul umístit.
1. Uvolněte modul a přemístěte jej do nové polohy.

### <a name="move-a-module-directly-within-the-canvas"></a>Přesuňte modul přímo na plátno

Chcete-li přesunout modul přímo v rámci plátna, postupujte následovně.

1. Vyberte modul, který chcete na plátně přesunout. 
1. Na panelu nástrojů modulu vyberte buď symbol šipky směřující nahoru nebo dolů a potom přetáhněte šipku na nové místo na stránce. Modrá čára v obrysu a na plátně označuje, kam lze modul umístit. Pokud nelze modul posunout nahoru nebo dolů, bude symbol šipky zobrazen šedě. 
1. Uvolněte modul a přemístěte jej do nové polohy.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Přesuňte modul pomocí nabídky se třemi tečkami

Chcete-li přesunout modul pomocí nabídky se třemi tečkami, postupujte takto.

1. Vyberte modul v obrysu nebo na plátně.
1. Vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu v podokně obrysu nebo na panelu nástrojů vybraného modulu na plátně.
1. Pokud lze modul pohybovat nahoru nebo dolů v kontejneru nebo slotu, zobrazí se možnosti pro **Posunout nahoru** nebo **Posunout dolů**. Vyberte požadovanou možnost přesunu pro přesun modulu nahoru nebo dolů vzhledem k jeho sourozencům.

## <a name="configure-modules"></a>Konfigurace modulů

Následující postupy popisují způsob konfigurace modulů obsahu a kontejneru.

### <a name="configure-a-content-module"></a>Konfigurace modulu obsahu

Chcete-li konfigurovat modul obsahu na stránce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo rozbalte stromovou strukturu a vyberte libovolný modul obsahu (například **Blok obsahu**). Případně vyberte modul, který chcete na hlavním plátně přesunout.
1. V podokně vlastností modulu vpravo zadejte vlastnosti pro všechny požadované ovládací prvky modulu.
1. Na příkazovém řádku vyberte možnost **Uložit**. Tím se také obnoví plátno náhledu.

### <a name="edit-module-text-properties"></a>Úprava textových vlastností modulu

Vlastnosti textu modulu, které nejsou jen pro čtení, lze upravovat přímo na plátně.

Chcete-li upravit vlastnosti textu modulu, postupujte takto.

1. Vyberte ovládací prvek textu na plátně a umístěte kurzor na místo, kde chcete text upravit.
1. Zadejte obsah textu.
1. Chcete-li pokračovat v úpravách jiného obsahu, vyberte místo kdekoli mimo textový obsah.

### <a name="inline-image-selection"></a>Výběr vloženého obrázku

Vlastnosti obrázku modulu, které nejsou jen pro čtení, lze měnit přímo na plátně.

Chcete-li zvolit nový obrázek pro modul obsahu, postupujte podle následujících kroků.

1. Na plátně dvakrát klikněte na obrázek. Otevře se okno pro výběr média.
1. Vyhledejte a vyberte nový obrázek, který chcete použít, a poté vyberte **OK**. Nový obrázek je nyní vykreslen na plátně.

### <a name="configure-a-container-module"></a>Konfigurace modulu kontejneru

Chcete-li konfigurovat modul kontejneru na stránce, postupujte podle následujících kroků.

1. Vyberte na stránce kontejnerový modul (například modul karuselového nebo tekutého kontejneru).
1. V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.
1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu kontejneru nebo slotu uvnitř kontejneru a pak vyberte **Přidat modul**. Poté přidejte do vybraného kontejneru podřízené moduly. Další informace naleznete v oddílu [Práce s moduly](#add-a-module) dříve v tomto tématu.
1. Pokud existuje více podřízených modulů v nadřazeném kontejneru na stejné úrovni, můžete změnit pořadí jejich zobrazení v nadřazeném kontejneru. Vyberte tlačítko se třemi tečkami pro modul a pak použijte tlačítka se šipkou nahoru a dolů.

## <a name="additional-resources"></a>Další zdroje

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)

[Práce s fragmenty](work-with-fragments.md)

[Přidání modulu kontejneru na stránku](add-container-module.md)

[Práce s publikovacími skupinami](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]