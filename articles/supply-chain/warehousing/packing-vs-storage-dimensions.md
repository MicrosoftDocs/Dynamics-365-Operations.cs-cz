---
title: Nastavení různých rozměrů pro balení a skladování
description: Tento článek ukazuje, jak určit, pro který proces (balení, skladování nebo vnořené balení) se použije každá zadaná dimenze.
author: Mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 85e40a0768174dcdc5d0fa2647b24cddccf01bdf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905479"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Nastavení různých dimenzí pro balení a skladování

[!include [banner](../../includes/banner.md)]

Některé položky jsou zabaleny nebo uloženy takovým způsobem, že budete možná muset sledovat fyzické dimenze odlišně pro každý z několika různých procesů. Funkce *Rozměry balení produktu* umožňuje nastavit jeden nebo několik typů dimenzí pro každý produkt. Každý typ dimenze poskytuje sadu fyzických měření (hmotnost, šířka, hloubka a výška) a zavádí proces, kde platí tyto hodnoty fyzického měření. Když je tato funkce povolena, systém bude podporovat následující typy dimenzí:

- *Úložiště* - Dimenze úložiště se používají společně s volumetrií umístění k určení, kolik z každé položky lze uložit v různých umístěních skladu.
- *Balení* - Dimenze balení se používají během kontejnerizace a procesu ručního balení k určení, kolik z každé položky se vejde do různých typů kontejnerů.
- *Vnořené balení* - Vnořené dimenze balení se používají, když proces balení obsahuje více úrovní.

*Dimenze úložiště* jsou podporovány, i když není funkce *Dimenze balení produktu* není povolena. Nastavíte je pomocí stránky **Fyzická dimenze** v Supply Chain Management. Tyto dimenze používají všechny procesy, kde nejsou specifikovány rozměry balení a vnořené rozměry.

Dimenze *Balení* a *vnořené balení* se nastavují pomocí stránky **fyzické dimenze produktu**, která se přidá, když povolíte funkci *Dimenze balení produktu*.
Tento článek poskytuje scénář, který ukazuje, jak používat tuto funkci.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Zapněte funkci dimenzí produktu balení

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Dimenze produktu balení*

## <a name="example-scenario"></a>Příklad

### <a name="set-up-the-scenario"></a>Nastavení scénáře

Než budete moci spustit ukázkový scénář, musíte připravit systém podle popisu v této části.

#### <a name="enable-demo-data"></a>Povolit ukázková data

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu *USMF*.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Přidání nové fyzické dimenze do produktu

Přidejte novou fyzickou dimenzi produktu pomocí následujícího postupu:

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt s **číslem položky** *A0001*.
1. V podokně akcí na kartě **Řízení zásob** a ve skupině **Sklad** vyberte **Fyzické rozměry produktu**.
1. Otevře se stránka **Fyzické rozměry produktu**. V podokně akcí vyberte možnost **Nový** pro přidání nové dimenze do mřížky s následujícím nastavením:
    - **Typ fyzické dimenze** - *Balení*
    - **Fyzická jednotka** - *ks*
    - **Váha** - *4*
    - **Hmotnost/jedn.** - *kg*
    - **Hloubka** - *3*
    - **Výška** - *4*
    - **Šířka** - *3*
    - **Délka** - *cm*
    - **Jednotka objemu** - *cm3*

Pole **Objem** se automaticky vypočítá na základě nastavení **Hloubka**, **Výška**, a **Šířka**.

#### <a name="create-a-new-container-type"></a>Vytvoření nového typu kontejneru

Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> typy kontejnerů** a vytvořte nový záznam s následujícím nastavením:

- **Typ kontejneru** - *Malá krabice*
- **Popis** - *Malá krabice*
- **Maximální čistá hmotnost** - *50*
- **Objem** - *144*
- **Délka** - *6*
- **Šířka** - *6*
- **Výška** - *4*

#### <a name="create-a-container-group"></a>Vytvoření skupiny kontejneru

Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> skupiny kontejnerů** a vytvořte nový záznam s následujícím nastavením:

- **ID skupiny kontejnerů** - *Malá krabice*
- **Popis** - *Malá krabice*

Přidejte nový řádek do oddílu **Detaily**. Nastavte **typ kontejneru** na *Malá krabice*.

#### <a name="set-up-a-container-build-template"></a>Nastavení šablony sestavení kontejneru

Jděte na **Řízení skladu \> Nastavení \> Kontejnery \> Šablony sestavení kontejneru** a vyberte **Krabice**. Změňte **ID skupiny kontejnerů** na *Malá krabice*.

### <a name="run-the-scenario"></a>Spuštění scénáře

Poté, co jste připravili svůj systém podle popisu v předchozí části, jste připraveni spustit scénář podle popisu v následující části.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Vytvoření prodejní objednávky a vytvoření zásilky

V tomto procesu vytvoříte zásilku na základě dimenzí *balení* položky, u nichž je výška menší než 3.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *63*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *5*

1. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
1. Zavřete stránku.
1. V podokně Akce na kartě **Sklad** otevřete možnost **Uvolnit do skladu**. Vytvoří se práce pro sklad.
1. Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad \> Podrobnosti o dodávce**.
1. V podokně akcí otevřete kartu **Doprava** a vyberte **Zobrazit kontejnery**. Potvrďte, že položka byla kontejnerizována do dvou kontejnerů *Malá krabice*.

#### <a name="place-an-item-into-storage"></a>Umístění položky do úložiště

1. Otevřete mobilní zařízení, přihlaste se do skladu 63 a přejděte na **Inventář \> Upravit**.
1. Zadejte **Loc** = *SHORT-01*. Vytvořte novou registrační značku pomocí **Položka** = *A0001* a **Množství** = *1 ks*.
1. Vyberte **OK**. Zobrazí se chyba „Umístění SHORT-01 se nezdařilo, protože položka A0001 se nevejde do zadaných rozměrů umístění.“ Důvodem je, že dimenze typu *Úložiště* produktu jsou větší než dimenze určené v profilu umístění.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]