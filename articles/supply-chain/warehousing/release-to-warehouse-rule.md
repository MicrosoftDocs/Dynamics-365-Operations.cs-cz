---
title: Pravidlo pro uvolnění do skladu
description: Toto téma uvádí informace o funkci Pravidlo pro uvolnění do skladu, jež zajišťuje určitou flexibilitu při provádění uvolnění do skladu. Doplňuje možnost konfigurovat, zda bude systém umožňovat uvolnění částečně rezervovaných řádků objednávek.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 2a9decad96f92450b9473ca10ccf7a98edf07a4316edd6d9ef92a70cc78c05ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716413"
---
# <a name="release-to-warehouse-rule"></a>Pravidlo pro uvolnění do skladu

[!include [banner](../includes/banner.md)]

Funkce *Pravidlo pro uvolnění do skladu* zajišťuje určitou flexibilitu při provádění uvolnění do skladu. Přidává novou možnost konfigurace pro každý jednotlivý sklad. Pomocí této možnosti můžete určit, zda má určitý sklad dovolit uvolnění částečně rezervovaných řádků objednávek. Tato funkce spolupracuje s funkcí rozšířeného cross dockingu v situacích, kdy je část množství z řádku objednávky označena již ve zdroji dodávky, ale zbývající část může je třeba zpracovat ve skladu. Řádek lze proto uvolnit, aby bylo možné pokračovat ve zpracování dostupného množství zásob ve skladu.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Zapnutí a inicializace funkce Pravidlo pro uvolnění do skladu

### <a name="turn-on-the-feature"></a>Zapnutí funkce

Než můžete použít funkci *Pravidlo pro uvolnění do skladu*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Pravidlo pro uvolnění skladu*

### <a name="initialize-the-feature"></a>Inicializace funkce

Po zapnutí funkce v systému je třeba ji inicializovat, aby se pravidlo nastavovalo do správného počátečního stavu pro všechny sklady.

- U skladů, u nichž není povoleno řízení skladů, má pravidlo ve výchozím nastavení hodnotu **Nelze použít**.
- U skladů, u nichž je povoleno řízení skladů, má pravidlo ve výchozím nastavení hodnotu **Povolit částečnou rezervaci**.

Chcete-li funkci inicializovat a pravidlo pro uvolnění do skladu nastavit pro všechny sklady, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na stránce **Parametry řízení skladu** vyberte na kartě **Všeobecné** v části **Informace o společnosti** odkaz na pravidlo **Inicializovat uvolnění do skladu**. (Pokud se tento odkaz nezobrazuje, není funkce zapnutá nebo již byla inicializována.)
1. Po zobrazení výzvy k potvrzení akce vyberte **Ano**. Provede se inicializace funkce.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Nastavení pravidla pro uvolnění do skladu pro jednotlivé sklady

Po zapnutí a inicializaci funkce budou všechny sklady ve výchozím nastavení popsaném v předchozí části. Toto nastavení můžete pro jednotlivé sklady měnit následujícím postupem.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Vyberte sklad, který chcete konfigurovat.
1. Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.
1. Na záložce s náhledem **Sklad** v části **Rezervace** určuje pole **Požadavek na rezervaci zásob**, zda je povoleno částečné uvolnění objednávek. Vyberte jednu z následujících hodnot:

    - **Nelze použít** – Když je funkce poprvé zapnuta a inicializována, přiřadí se automaticky všem skladům, u nichž není řízení skladu povoleno, tato hodnota. Tento údaj nelze změnit. Tato hodnota není dostupná pro sklady, u nichž je řízení skladů povoleno.
    - **Povolit částečnou rezervaci** – objednávky lze uvolnit, když je rezervováno jakékoli množství. Systém vyhodnotí, zda by mělo být nerezervované množství označeno pro rozšířený cross docking a toto množství dle potřeby označí. Pokud žádné označení neexistuje, systém vytvoří práci pouze pro rezervované množství. Když je funkce poprvé zapnuta a inicializována, přiřadí se automaticky všem skladům, u nichž je řízení skladu povoleno, tato hodnota. Tato hodnota není dostupná pro sklady, u nichž není řízení skladů povoleno.
    - **Vyžadovat úplnou rezervaci** – objednávky lze uvolnit pouze v případě, že je rezervováno celé množství. Objednávky nelze uvolnit, pokud celkové množství není fyzicky rezervováno nebo naplánováno pro cross docking. Tato hodnota není dostupná pro sklady, u nichž není řízení skladů povoleno.

1. Zvolte **Uložit**.

## <a name="scenarios"></a>Scénáře

Tato část obsahuje dva scénáře, pomocí kterých se můžete naučit, co tato funkce provádí a jak ji lze využívat.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s těmito scénáři pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tyto scénáře můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému. V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Scénář 1: Vyžadovat úplné uvolnění (bez plánovaného cross dockingu)

Tento scénář ukazuje, jak tato funkce funguje pro sklady, u nichž je nastavena možnost **Vyžadovat úplnou rezervaci**.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Pro sklad _62_, nastavte v poli **Požadavek na rezervaci zásob** hodnotu **Vyžadovat úplnou rezervaci**, jak se popisuje v části [Nastavení pravidla pro uvolnění do skladu pro jednotlivé sklady](#set-option-warehouse) tohoto tématu.
1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu _US-004_.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu _62_.

1. Vyberte **OK**, nová prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Zahrnuje prázdný řádek v mřížce v části **Řádky prodejních objednávek**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *A0001*
    - **Množství:** *2*

1. Chcete-li přidat nový řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *A0002*
    - **Množství:** *2*

1. Vyberte první řádek objednávky a poté v nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. Neprovádějte rezervaci pro druhý řádek objednávky.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.
1. Zobrazí se následující chybová zpráva: „Vždy je nutné rezervovat úplné množství.“ Systém proto pro objednávku nevytvoří práci, dodávku ani náklad.

    > [!NOTE]
    > Pokud provedete částečnou rezervaci druhého řádku, zobrazí se stejná chybová zpráva.

### <a name="scenario-2-allow-partial-release"></a>Scénář 2: Povolení částečného uvolnění

Tento scénář ukazuje, jak tato funkce funguje pro sklady, u nichž je nastavena možnost **Povolit částečné uvolnění**.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Pro sklad _62_, nastavte v poli **Požadavek na rezervaci zásob** hodnotu **Povolit částečnou rezervaci**, jak se popisuje v části [Nastavení pravidla pro uvolnění do skladu pro jednotlivé sklady](#set-option-warehouse) tohoto tématu.
1. Podobně jako v [předchozím scénáři](#scenario1) přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky** a vytvořte prodejní objednávku pro účet odběratele _US-004_ ze skladu _62_. Přidejte následující dva řádky objednávky:

    - **Řádek 1:** Nastavte v poli **Číslo položky** hodnotu _A0001_, v poli **Množství** hodnotu _2_ a v poli **Jednotka** hodnotu _ks_.
    - **Řádek 2:** Nastavte v poli **Číslo položky** hodnotu _A0002_, v poli **Množství** hodnotu _2_ a v poli **Jednotka** hodnotu _ks_.

1. Podobně jako v [předchozím scénáři](#scenario1) rezervujte úplné množství pro řádek 1 objednávky, ale neprovádějte rezervaci pro řádek 2.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.
1. Všimněte si, že se tentokrát žádná chybová zpráva nezobrazí. Místo toho systém podle potřeby vytvoří práci, dodávky a náklady a zobrazí příslušné výsledky.
1. Chcete-li zobrazit informace o dodávce, nákladu a práci, použijte možnosti z nabídky **Sklad** nad mřížkou:

    - **Řádek 1:** K dispozici jsou tři možnosti: **Podrobnosti dodávky**, **Podrobnosti nákladu** a **Podrobnosti práce**. Výběrem jednotlivých možností zobrazíte podrobnosti o dodávce, nákladu a práci. Tyto položky byly vytvořeny při uvolnění objednávky do skladu.
    - **Řádek 2:** K dispozici je pouze možnost **Podrobnosti práce**. Vyberte ji a všimněte si, že nebyla vytvořena žádná práce, protože nebyly rezervovány žádné zásoby. Proto se nevytvořila žádná dodávka ani náklad.

> [!NOTE]
> Stejný výsledek lze očekávat, když bude druhý řádek částečně rezervován. V tomto případě se vytvoří práce rezervované množství řádku objednávky, nikoli však pro množství pro něž rezervace provedena nebyla.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]