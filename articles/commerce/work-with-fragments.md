---
title: Práce s fragmenty
description: V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98cb1fba158ea99427d2068ca49b257cb5290de3
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090737"
---
# <a name="work-with-fragments"></a>Práce s fragmenty 

[!include [banner](includes/banner.md)]

V tomto tématu jsou popsány důvody, kdy a jak používat fragmenty v aplikaci Microsoft Dynamics 365 Commerce.

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

![Na obrázku je znázorněno, jak lze fragmenty použít k centralizaci vytváření konfigurací sdílených modulů v rámci webu e-Commerce..](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Vytvořit fragment

Můžete vytvořit nový fragment nebo uložit existující konfiguraci modulu jako fragment.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Uložit existující konfiguraci modulu jako fragment

Chcete-li převést dříve konfigurovaný modul na opakovaně použitelný fragment v tvůrci webů Commerce, postupujte následujícím způsobem.

1. Otevřete stránku nebo šablonu obsahující modul, který chcete převést na fragment.
1. V podokně osnovy vlevo nebo přímo ve vizuálním tvůrci stránek vyberte dříve nakonfigurovaný modul.
1. Vyberte tlačítko se třemi tečkami (**...**) vedle názvu modulu v podokně osnovy nebo na panelu nástrojů vybraného modulu ve vizuálním tvůrci stránek. 
1. Vyberte možnost **Sdílet jako fragment**. 
1. V dialogovém okně **Uložit jako fragment** zadejte název fragmentu.
1. Chcete-li uložit konfiguraci modulu jako fragment, který lze přidat na jiné stránky, klepněte na tlačítko **OK**.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Vytvořit nový fragment

Nový fragment vytvoříte v konfigurátoru webů Commerce tímto postupem.

1. V navigačním podokně nalevo vyberte položku **Fragmenty**.
1. Zvolte **Nové**. Zobrazí se dialogové okno **Nový fragment** s informacemi o všech dostupných typech modulů. Jak bylo zmíněno dříve, fragmenty mohou být vytvořeny z libovolného typu modulu.
1. Vyberte typ modulu pro váš fragment.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Výběrem generického typu kontejnerového modulu získáte maximální pružnost při aktualizaci a konfiguraci fragmentu později.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Přidání, odebrání nebo úprava fragmentů na stránce

Následující postupy popisují způsob přidávání, odebírání a úprav fragmentů.

### <a name="add-a-fragment"></a>Přidat fragment

Fragment přidáte na stránku v konfigurátoru webů Commerce tímto postupem.

1. V podokně osnovy vlevo nebo přímo ve vizuálním tvůrci stránek vyberte kontejner nebo slot, do kterých lze přidávat podřízené moduly.
1. Vyberte tři tečky (**...**) vedle názvu kontejneru nebo slotu.  Případně, pokud používáte vizuální tvůrce stránek, vyberte symbol plus (**+**).  
1. Vyberte **Přidat fragment**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat fragment** k dispozici.
    
1. V dialogovém okně **Vybrat fragment** vyhledejte a vyberte fragment, který chcete přidat. Nejsou-li v seznamu uvedeny žádné fragmenty, bude pravděpodobně nutné nejprve vytvořit fragment z typu modulu, který podporuje vybraný kontejner nebo slot.
1. Výběrem přidáte požadovaný fragment do vybraného kontejneru nebo slotu na stránce.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Moduly, které jsou povoleny v kontejneru nebo slotu, jsou definovány šablonou stránky nebo vlastními definicemi modulů.

### <a name="remove-a-fragment"></a>Odebrání fragmentu

Chcete-li odebrat fragment ze slotu nebo kontejneru na stránce v tvůrci webů Commerce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami (**...**) vedle názvu fragmentu, který chcete odebrat, a pak vyberte symbol odpadkového koše.  Alternativně můžete vybrat fragment ve vizuálním tvůrci stránek a vybrat symbol koše na panelu nástrojů fragmentu.
1. Až budete vyzváni k potvrzení odebrání fragmentu, vyberte **OK.**

> [!NOTE]
> Odeberete-li fragment ze stránky, odstraníte z něj pouze odkaz na něj. **Neodstraníte** fragment z vašeho webu. Chcete-li odstranit fragmenty z webu, je nutné použít uživatelské rozhraní inspektoru fragmentů. Fragmenty z webu lze odstranit pouze v případě, že na ně aktuálně neodkazují žádné stránky, šablony nebo jiné fragmenty.

### <a name="edit-a-fragment"></a>Upravit fragment

Chcete-li upravit fragmenty, je nutné použít uživatelské rozhraní editoru fragmentů. Toto omezení je záměrné. Pomáhá zajistit, aby autoři neměnili proces úpravy modulů pro konkrétní stránku s procesem úprav fragmentů, které mohou být sdíleny na více stránkách.

Fragment upravíte v konfigurátoru webů Commerce tímto postupem.

1. V navigačním podokně nalevo vyberte položku **Fragmenty**.
1. Mezi **Fragmenty** vyberte fragment, který chcete upravit.
1. Upravte vlastnosti a strukturu modulu fragmentu podle potřeby. Proces se podobá procesu úpravy modulů v zobrazení editoru stránek.

Fragment můžete také upravit tak, že jej vyberete na stránce, v šabloně nebo v nadřazeném fragmentu a poté vyberete **Upravit fragment** v podokně vlastností vpravo.

### <a name="rename-a-fragment"></a>Přejmenování fragmentu

Stávající fragment přejmenujete v konfigurátoru webů tímto postupem.

1. V levém navigačním podokně vyberte položku **Fragmenty**.
1. Vyberte název fragmentu, který chcete změnit.
1. Výběrem příkazu **Upravit** začněte úpravu fragmentu. Upozorňujeme, že fragment nelze upravit, pokud jej již upravuje někdo jiný.
1. V podokně vlastností fragmentu vyberte symbol pera vedle názvu fragmentu.
1. Podle potřeby upravte název fragmentu.
1. Zaškrtnutím políčka potvrďte změnu názvu.
1. Vyberte **Dokončit úpravy**.

Fragment můžete po jeho vytvoření přejmenovat tak, že jej upravíte a poté vyberete symbol pera vedle názvu fragmentu v panelu vlastností.

## <a name="additional-resources"></a>Další prostředky

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)

[Práce se skupinami publikování](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
