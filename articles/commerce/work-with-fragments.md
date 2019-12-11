---
title: Práce s fragmenty
description: V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698089"
---
# <a name="work-with-fragments"></a>Práce s fragmenty 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Fragmenty umožňují centralizované prostředí pro vytváření konfigurací modulu, které je nutné znovu použít v celém webu. Například záhlaví, zápatí a nápisy jsou často konfigurovány jako fragmenty, protože jsou sdíleny na více stránkách. Fragmenty lze považovat za miniaturní webové stránky, které lze vložit do jiných stránek na vašem webu. Fragmenty mají vlastní životní cyklus. Jinými slovy, jsou vytvořeny, odkazovány, aktualizovány a odstraněny jako nezávislé entity ve vývojových nástrojích.

Po dokončení konfigurace fragmentů lze použít všechny moduly, které mohou být použity ve struktuře webu. Fragmenty mohou odkazovat na stránkách, v rozvržení, v šablonách a v jiných fragmentech.

> [!NOTE]
> Fragmenty mohou být vnořeny do sedmi úrovní v jiných fragmentech.

Chcete-li například propagovat velké množství stránek na více stránkách na našem webu, můžete použít fragment. Prvním krokem při vytváření nového fragmentu je výběr typu modulu, ze kterého chcete začít. V tomto příkladu můžete vytvořit fragment z modulu Hero.

> [!NOTE]
> Fragmenty mohou být vytvořeny z libovolného typu modulu.

Poté můžete nakonfigurovat fragment Hero s konkrétním reklamním obsahem. Můžete jej také lokalizovat podle potřeby. Nový fragment Hero může být poté spotřebován jako předkonfigurovaný modul na vašem webu. Lze jej snadno přidat do šablon, na určité stránky nebo do jiných fragmentů, které mohou obsahovat Hero moduly.

Všechna místa, kde je fragment přidán, jsou odkazy na vytvořený centrální fragment Hero. Pokud publikujete změny ve fragmentu, tyto změny se okamžitě projeví ve všech místech, kde je fragment odkazován na celém webu. Proto fragmenty poskytují výkonný a účinný prostředek pro opětovné použití a centrální správu konfigurací modulů na pracovišti. Pomocí těchto funkcí můžete významně zvýšit pružnost a snížit náklady, které jsou spojeny s řízením obsahu webu.

Na následujícím obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.

![Na obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Vytvořit fragment

Můžete vytvořit nový fragment nebo uložit existující konfiguraci modulu jako fragment.

### <a name="create-a-new-fragment"></a>Vytvořit nový fragment

Při vytváření nového fragmentu postupujte takto:

1. V navigačním podokně nalevo vyberte položku **Fragmenty**.
1. Zvolte **Nový fragment stránky**. Zobrazí se dialogové okno s informacemi o všech dostupných typech modulů. Jak bylo zmíněno dříve, fragmenty mohou být vytvořeny z libovolného typu modulu.
1. Vyberte typ modulu pro svůj fragment a poté klepněte na tlačítko **OK**.

    > [!TIP]
    > Výběrem generického typu kontejnerového modulu získáte maximální pružnost při aktualizaci a konfiguraci fragmentu později.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Uložit existující konfiguraci modulu jako fragment

Chcete-li převést dříve konfigurovaný modul na opakovaně použitelný fragment, postupujte následujícím způsobem.

1. Otevřete stránku nebo šablonu obsahující modul, který chcete převést na fragment.
1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu a pak vyberte možnost **Uložit jako fragment.** Zobrazí se dialogové okno.
1. Zadejte název a metadata fragmentu.
1. Chcete-li uložit konfiguraci modulu jako fragment, který lze přidat na jiné stránky, klepněte na tlačítko **OK**.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Přidání, odebrání nebo úprava fragmentů na stránce

Následující postupy popisují způsob přidávání, odebírání a úprav fragmentů.

### <a name="add-a-fragment"></a>Přidat fragment

Chcete-li přidat fragment na stránku, postupujte takto:

1. V podokně osnovy vlevo vyberte kontejner nebo slot, do kterých lze přidávat podřízené moduly.
1. Vyberte tlačítko se třemi tečkami názvu kontejneru nebo slotu a poté vyberte možnost **Přidat fragment**. Zobrazí se dialogové okno.

    > [!NOTE]
    > Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat fragment** k dispozici.

1. V dialogovém okně vyhledejte a vyberte fragment, který chcete přidat. Nejsou-li v seznamu uvedeny žádné fragmenty, bude pravděpodobně nutné nejprve vytvořit fragment z typu modulu, který podporuje vybraný kontejner nebo slot.
1. Výběrem tlačítka **OK** přidáte vybraný fragment do vybraného kontejneru nebo slotu na stránce.

> [!NOTE]
> Moduly, které jsou povoleny v kontejneru nebo slotu, jsou definovány šablonou stránky nebo vlastními definicemi modulů.

### <a name="remove-a-fragment"></a>Odebrání fragmentu

Chcete-li odebrat fragment ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu modulu, který chcete odebrat, a pak vyberte tlačítko odpadkového koše.
1. Až budete vyzváni k potvrzení odebrání fragmentu, vyberte **OK.**

> [!NOTE]
> Odeberete-li fragment ze stránky, odstraníte z něj pouze odkaz na něj. **Neodstraníte** fragment z vašeho webu. Chcete-li odstranit fragmenty z webu, je nutné použít uživatelské rozhraní inspektoru fragmentů. Fragmenty z webu lze odstranit pouze v případě, že na ně aktuálně neodkazují žádné stránky, šablony nebo jiné fragmenty.

### <a name="edit-a-fragment"></a>Upravit fragment

Chcete-li upravit fragmenty, je nutné použít uživatelské rozhraní editoru fragmentů. Toto omezení je záměrné. Pomáhá zajistit, aby autoři neměnili proces úpravy modulů pro konkrétní stránku s procesem úprav fragmentů, které mohou být sdíleny na více stránkách.

Při editaci fragmentu postupujte takto:

1. V navigačním podokně nalevo vyberte položku **Fragmenty**.
1. Mezi **Fragmenty** vyberte fragment, který chcete upravit.
1. Upravte vlastnosti a strukturu modulu fragmentu podle potřeby. Proces se podobá procesu úpravy modulů v zobrazení editoru stránek.

Fragment můžete také upravit tak, že jej vyberete na stránce, v šabloně nebo v nadřazeném fragmentu a poté vyberete **Upravit fragment** v podokně vlastností vpravo.

## <a name="additional-resources"></a>Další zdroje

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)
