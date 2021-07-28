---
title: Povolení a konfigurace automatických nákladů podle kanálu
description: V tomto tématu je vysvětleno, jak povolit a konfigurovat automatické náklady podle kanálu v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: c38717ca9c57913ea22f2dd7712b49f39d2e556e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349691"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Povolení a konfigurace automatických nákladů podle kanálu

V tomto tématu je vysvětleno, jak povolit a konfigurovat automatické náklady (auto náklady) podle kanálu v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Je možné, že používáte scénáře, ve kterých je nutné použít náklady za recyklaci nebo jiné náklady pro skupinu produktů prodávaných ve všech nebo v některých prodejnách v určitém stavu (například Kalifornie). Funkce **Povolit automatické náklady filtru podle kanálů** v modulu Commerce vám umožní určit automatické náklady podle kanálu (například konkrétní kanál kamenného obchodu). Tato funkce je k dispozici v Dynamics 365 Commerce verze 10.0.10 a novější.

Chcete-li povolit a konfigurovat automatické náklady podle kanálu, je nutné provést následující úkony:

- Zapněte funkci **Povolit automatické náklady filtru podle kanálu**.
- Konfigurujte účel organizační hierarchie.
- Definovat automatické náklady podle kanálu.

> [!NOTE]
> Funkce **Povolit automatické náklady filtru podle kanálů** funguje pouze v případě, že je zapnuta také funkce Rozšířené automatické náklady. Informace o tom, jak zapnout funkci rozšířené náklady, naleznete v tématu [Omnikanál – pokročilé automatické náklady](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Zapněte funkci Povolit automatické náklady filtru podle kanálu

Chcete-li povolit automatické náklady podle kanálu v Commerce, postupujte podle následujících kroků.

1. Přejděte do nabídky **Správce systému \> Pracovní prostory \> Správa funkcí**.
1. Na kartě **Nepovoleno** v seznamu **Název funkce** najděte a vyberte možnost **Povolit filtrování automatických poplatků podle kanálu.**
1. V pravém dolním rohu vyberte možnost **Povolit nyní.** Jakmile je funkce zapnuta, zobrazí se v seznamu na kartě **Vše**.
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. V levém podokně vyhledejte a vyberte úlohu **1110** (**globální konfigurace**).
1. V podokně akcí vyberte možnost **Spustit nyní** a rozšiřte změny konfigurace.

> [!WARNING]
> Pokud vypnete funkci **Automatické náklady filtru po kanálech** po jejím použití, pole **Vztah maloobchodní sítě** v části **Automatické náklady** se již nezobrazí a všechny existující konfigurace budou ztraceny. Pokud odebrání konfigurací **Vztah maloobchodní sítě** způsobí, že budou pravidla pro automatické náklady duplikována, pokus o vypnutí této funkce se nezdaří. Před vypnutím funkce zkontrolujte všechna pravidla automatických poplatků a proveďte požadované změny.

## <a name="configure-the-organization-hierarchy-purpose"></a>Konfigurujte účel organizační hierarchie

Byl vytvořen nový účel hierarchie organizace, který se nazývá **Maloobchodní auto poplatek** za účelem správy hierarchie pro automatické náklady podle kanálu.

Chcete-li přiřadit výchozí hierarchii k účelu organizační hierarchie v Commerce, postupujte takto.
        
1. Přejděte do nabídky **Správa organizace \> Organizace \> Účely organizační hierarchie**.
1. V levém podokně vyberte možnost **Automatické náklady maloobchodu**.
1. V části **Přiřazené hierarchie** vyberte **Přidat**.
1. V dialogovém okně **Organizační hierarchie** vyberte organizační hierarchii (naříklad **Maloobchody podle regionu**) a poté vyberte **OK**.
1. V části **Přiřazené hierarchie** vyberte **Nastavit jako výchozí**.
1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. V levém podokně vyhledejte a vyberte úlohu **1040** (**Produkty**).
1. V podokně akcí zvolte **Spustit nyní**.
1. Zopakováním předchozích dvou kroků spusťte úlohy **1070** (**Konfigurace kanálů**) a **1110** (**globální konfigurace**).

![Konfigurace maloobchodního automatického poplatku účel organizační hierarchie.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Definovat automatické náklady podle kanálu

Po zapnutí funkce **Povolit automatické náklady filtru podle kanálů** a nakonfigurování organizační hierarchie **Maloobchodní automatický poplatek** lze automatické náklady podle kanálu definovat buď na úrovni záhlaví objednávky nebo na úrovni řádku objednávky.

Chcete-li definovat automatické náklady podle kanálu v Commerce, postupujte podle následujících kroků.

1. Přejděte na **Pohledávky \> Nastavení nákladů \> Automatické náklady**.
1. V levém podokně v poli **Úroveň** vyberte možnost **Záhlaví** nebo **Řádek** podle požadavků na obchod.
1. V poli **Kód maloobchodní sítě** vyberte příslušný kód kanálu (například **tabulka** nebo **skupina**). Je-li použita výchozí hodnota **Vše**, použijí se pravidla poplatků pro všechny kanály.

    - Pokud vyberete **Skupina**, ujistěte se, že je vytvořena skupina poplatků maloobchodních kanálů v **Retail and Commerce \> Nastavení kanáků \> Náklady \> Skupiny nákladů maloobchodních kanálů**.
    - Pokud vyberete možnost **Tabulka**, můžete vybrat určitý kanál (například **San Francisco**) v poli **Vztah maloobchodních kanálů**.

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. V levém podokně vyhledejte a vyberte úlohu **1040** (**Produkty**).
1. V podokně akcí zvolte **Spustit nyní**.
1. Zopakováním předchozích dvou kroků spusťte úlohy **1070** (**Konfigurace kanálů**) a **1110** (**globální konfigurace**).
    
![Automatické náklady definované podle kanálu.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Příklad

Následující příklad popisuje kroky, které jsou nutné ke konfiguraci produktu tak, aby byly náklady za recyklaci účtovány při prodeji produktu prostřednictvím kamenného obchodu v San Franciscu. V příkladu se také zobrazuje způsob zobrazení automatických nákladů v aplikaci pokladní místo (POS) Commerce.

Organizace definuje kód nákladů, který se nazývá **RECYKLACE**, jak je znázorněno na následujícím obrázku.

![Kód nákladů RECYKLACE.](media/Auto-charges-charge-code.png)

Vytvoří se automatické náklady na úrovni řádku. Má následující konfiguraci:

- Pole **Kód účtu** je nastaveno na **Vše**.
- Pole **Kód položky** je nastaveno na **Tabulka**.
- Pole **Vztah položky** je nastaveno na ID produktu **91001**.
- Pole **Kód způsobu dodání** je nastaveno na **Vše**.
- Pole **Kód maloobchodní sítě** je nastaveno na **Tabulka**.
- Pole **Vztah maloobchodních kanálů** je nastaveno na obchod **San Francisco**.

Je vytvořen řádek automatických nákladů. Má následující konfiguraci:

- Pole **Měna** je nastaveno na hodnotu **USD**.
- Pole **Kód nákladů** je nastaveno na **RECYKLACE**.
- Pole **Kategorie** je nastaveno na hodnotu **Pevná**.
- Pole **Náklady** je nastaveno na **$ 6,25**.

![Konfigurace automatického nákladu na úrovni řádku a řádku automatických nákladů.](media/Auto-charges-recyclingfee-line-fee.png)

V aplikaci POS se vytvoří prodejní objednávka v kanálu obchodu **San Francisco**. Řádek **Náklady** zobrazuje poplatek za recyklaci **$6,25.**

Výběrem **Možnosti transakce \> Náklady \> Správa nákladů** v aplikaci POS můžete zobrazit kód nákladů a popis poplatku za recyklaci.

![Poplatek za recyklaci v aplikaci POS.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Další prostředky

[Omnikanálové rozšířené automatické náklady](omni-auto-charges.md)

[Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]