---
title: Mezipodnikové plánování
description: Tento článek popisuje mezipodnikové plánování a vysvětluje, jak nakonfigurovat mezipodnikové plánování pomocí optimalizace plánování v Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c13ecca9523707ef3df5fdb97dc4cbd79478258d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850663"
---
# <a name="intercompany-planning"></a>Mezipodnikové plánování

[!include [banner](../../includes/banner.md)]

U některých organizací závisí logistické operace na jiných právnických osobách (společnostech) v organizaci. Tyto operace jsou zpracovávány pomocí mezipodnikových prodejů a nákupů, protože každá právnická osoba má samostatnou účtovou osnovu.

Tento článek popisuje mezipodnikové plánování a vysvětluje, jak nakonfigurovat mezipodnikové plánování pomocí optimalizace plánování v Microsoft Dynamics 365 Supply Chain Management.

Tento článek používá následující důležité mezipodnikové výrazy:

- **Směrem k dodavateli** - Relativní reference ve firmě nebo dodavatelském řetězci. Indikuje pohyb ve směru k dodavateli suroviny.
- **Směrem ke spotřebiteli** - Relativní reference ve firmě nebo dodavatelském řetězci. Indikuje pohyb ve směru k zákazníkovi.
- **Plánovaná mezipodniková poptávka** - Plánovaná poptávka po produktu ve společnosti na základě plánované poptávky po produktu od navazující společnosti.

V hlavním plánování může plán v jedné společnosti zahrnovat plánovanou mezipodnikovou poptávku, která souvisí s plánovanými objednávkami z plánu v jiné společnosti. Tato funkce je užitečná, protože poskytuje úplný přehled o plánovaných objednávkách napříč společnostmi. Zajišťuje také, že jsou vytvořeny všechny požadované plánované objednávky dodávek, ale bez požadavku, aby byly plánované objednávky zpracovány pro mezipodnikovou poptávku.

Pokud spustíte hlavní plánování z hlavního plánu, který zahrnuje plánovanou následnou poptávku, plánované nákupní objednávky od příslušných mezipodnikových dodavatelů budou zahrnuty do plánu jako poptávka.

## <a name="required-setup"></a>Požadované nastavení

Chcete-li použít mezipodnikové plánování, musíte svůj systém připravit následujícím způsobem:

1. Příslušné produkty musí být uvolněny ve všech příslušných společnostech. Další informace naleznete v tématu [Konfigurace a použití mezipodnikového obchodu v Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) na Microsoft Learn.
1. Následná poptávka musí být pokryta nákupy od dodavatele, který má mezipodnikový vztah k předcházející společnosti a relevantní výchozí dimenze zásob (pracoviště a sklad) na zákazníkovi. Další informace naleznete v tématu [Konfigurace a použití mezipodnikového obchodu v Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) na Microsoft Learn.
1. Hlavní plán v předcházející společnosti musí zahrnovat plánovanou následnou poptávku a příslušná společnost a hlavní plán musí být specifikovány v následných plánech.

## <a name="include-planned-downstream-demand"></a>Zahrnout podřízenou plánovanou poptávku

Podle těchto pokynů nakonfigurujte svůj hlavní plán tak, aby zahrnoval plánovanou následnou poptávku.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte nebo vytvořte hlavní plán.
1. Na záložce s náhledem **Mezipodnikové plánování** zadejte následující pole:

    - **Zahrnout plánovanou následnou poptávku** - Nastavte tuto možnost na *Ano*, čímž umožníte mezipodnikové plánování pro hlavní plán.
    - **Následné plány** - Pokud nastavíte možnost **Zahrnout plánovanou následnou poptávku** na *Ano*, použijte panel nástrojů a mřížku a přidejte požadované hlavní plány od jiných společností.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Dokládání napříč společnostmi pomocí víceúrovňového doložení

Ve víceúrovňovém doložení můžete zobrazit doložení napříč společnostmi, abyste viděli počáteční zdroj poptávky, který je krytý nabídkou.

Chcete-li zobrazit informace o víceúrovňovém doložení, postupujte takto.

1. Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**.
1. Vyberte nebo otevřete plánovanou objednávku.
1. V podokně akcí na kartě **Zobrazit** ve skupině **Požadavky** vyberte **Víceúrovňové doložení**.

### <a name="intercompany-example-that-involves-two-companies"></a>Mezipodnikový příklad, který zahrnuje dvě společnosti

V tomto příkladu je ve společnosti USMF vytvořena plánovaná výrobní zakázka, která pokryje prodejní objednávku ve společnosti DEMF. V USMF je přímá poptávka plánovanou mezipodnikovou poptávkou. Aby se tato poptávka objevila v USMF, je hlavní plánování spuštěno nejprve v DEMF a poté v USMF.

Následující ilustrace ukazuje, jak by se tento příklad mohl objevit na stránce **Víceúrovňové zakotvení** pro plánovanou výrobní zakázku.

![Mezipodnikový příklad, který zahrnuje dvě společnosti.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Mezipodnikový příklad, který zahrnuje tři společnosti

V tomto příkladu je ve společnosti USMF vytvořena plánovaná nákupní objednávka, která pokryje prodejní objednávku ve společnosti FRRT. Ve společnostech DEMF a USMF je přímá poptávka plánovanou mezipodnikovou poptávkou. Aby se tato poptávka objevila v USMF, je hlavní plánování spuštěno nejprve v FRRT, poté v DEMF a nakonec v USMF.

Následující ilustrace ukazuje, jak by se tento příklad mohl objevit na stránce **Víceúrovňové zakotvení** pro plánovanou výrobní zakázku.

![Mezipodnikový příklad, který zahrnuje tři společnosti.](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]