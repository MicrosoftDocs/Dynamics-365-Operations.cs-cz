---
title: Přehled účetních profilů
description: Tento článek vysvětluje, jak se ve všech aplikacích Microsoft Dynamics 365 používají profily účtování.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876117"
---
# <a name="posting-profiles-overview"></a>Přehled účetních profilů

V aplikacích Finance a Operace se termín *profily účtování* používá k popisu konfigurací, které řídí, jak se účty vedlejší knihy převádějí na hlavní účty, aby je bylo možné použít v transakcích zaúčtovaných do hlavní knihy. Řídí například, jak se zákazník při zaúčtování faktury převede na hlavní účet pohledávek.

Některé moduly a funkce mají stránku, která v názvu obsahuje slova „profil účtování“ (např. **Profil účtování zákazníka** nebo **Profil účtování dodavatele**). Některé moduly mají navíc více možností pro konfiguraci účtování v hlavní knize pro transakce, které jsou generovány z vedlejší knihy. Například v modulu **Kontrola produkce** můžete nastavit účtování podle produkční skupiny, zdroje nebo skupiny zdrojů.

Pro mnoho typů transakcí existuje alternativa k profilům účtování: definice účtování. U podporovaných dokumentů můžete ke klasifikaci hlavních účtů a finančních dimenzí účetních položek použít namísto účetních profilů definice účtování. Pokud plánujete používat věcné břemeno nebo předběžná břemena, je pro definování účtů pro účetní zápisy vyžadována definice účtování.

Než budete moci nakonfigurovat profily odesílání, definice odesílání nebo stránku **Účty pro automatické transakce**, musíte nakonfigurovat účtovou osnovu na stránce **Hlavní kniha** v právnické osobě, kterou chcete konfigurovat.

## <a name="posting-types"></a>Typ zaúčtování

V aplikacích Finance a Operace se typ účtování používá k definování obecné kategorie pro debet nebo kredit. Tato kategorie je nezávislá na hlavním účtu v hlavní knize. V hlavní knize existují typy účtování pro každý debet nebo kredit.

Jeden doklad může mít jeden nebo více typů zaúčtování. Například transakce, která je zaúčtována prostřednictvím obecného deníku, kde jsou nastaveny účet a kompenzační účet na **Hlavní kniha**, bude mít typ účtování **Hlavní deník** pro debet i kredit. Naproti tomu faktura dodavatele bude mít více typů účtování. Tyto typy účtování budou zahrnovat jeden řádek pro zůstatek dodavatele a další řádky pro kompenzační záznam, jako je např. **Hlavní deník**.

Můžete zobrazit typ účtování v poli **Typ účtování** na kartě **Všeobecné** stránky **Transakce dokladů** strana.

> [!TIP]
> Můžete použít panel nástrojů **Přizpůsobení** pro přidání pole **Typ účtování** k mřížce na kartě **Přehled** kartu nebo jeho přesunu. Tímto způsobem můžete usnadnit přístup k tomuto poli nebo jeho zobrazení při prohlížení dokladů.

## <a name="detail-settings-for-a-posting-profile"></a>Detailní nastavení pro profil účtování 

Když konfigurujete profily účtování, pole **Kód účtu** definuje úroveň nastavení. K dispozici jsou následující možnosti: **Tabulka**, **Skupina** a **Vše**. Shoda se zastaví po první shodě a pořadí je od nejkonkrétnější úrovně po nejméně konkrétní úroveň. Ačkoliv pole **Kód účtu** může mít v některých případech mírně odlišný název, chování a funkce pole zůstávají stejné. Například profil účtování zásob obsahuje pole **Kód položky** a pole **Kód účtu**. Obě pole mají hodnoty **Tabulka**, **Skupina** a **Vše**.

Pokud je pole **Hlavní účet** ponecháno prázdné pro profil odesílání a nenakonfigurovali jste hlavní účet na stránce **Účty pro automatické transakce** nebo na stránce specifické pro modul nebo funkci, obdržíte chybovou zprávu, když zaúčtujete transakci, která používá typ účtování. Obvykle bude zpráva vypadat následovně: „Účet pro \[Typ účtování\] nelze najít.“

### <a name="table-value"></a>Hodnota tabulky

Hodnota **Tabulka** odkazuje na hlavní záznam, který je přidružen k profilu účtování. Každý záznam tabulky je specifický pro jednu hodnotu. Tuto hodnotu zadáte do pole, které se zobrazí za polem **Kód účtu**. Toto pole je obvykle pojmenováno **Účet** nebo **Číslo účtu/skupiny**. Přesný název se liší v závislosti na stránce, kde se vyskytuje.

Pokud například pracujete s profilem účtování zákazníků, hodnota **Tabulka** představuje konkrétního zákazníka. Proto pokud jste v poli **Kód účtu** vybrali možnost **Tabulka**, musíte vybrat číslo zákazníka v poli **Číslo skupiny/účtu**.

Hodnota **Tabulka** představuje nejkonkrétnější typ záznamu. Systém vždy používá tuto hodnotu, i když jste nakonfigurovali jiný záznam, kde je vybrána hodnota **Skupina** nebo **Vše**. Tato hodnota také přepíše všechny hodnoty, které jste vytvořili jako výchozí hodnoty na stránce **Účty pro automatické transakce**.

Nedoporučujeme vám používat hodnotu **Tabulka** jako primární mechanismus pro správu vašich profilů účtování, protože problémy s kvalitou dat mohou nastat, pokud je pro každý záznam kmenových dat udržován samostatný profil účtování. Je také obtížné udržovat a sladit samostatný profil účtování pro každý záznam hlavních dat. Místo toho by tato hodnota měla být použita ke správě výjimek ve vašich profilech odesílání.

### <a name="group-value"></a>Hodnota skupiny

Hodnota **Skupina** odkazuje na seskupovací záznam, který je podporován hlavním záznamem přidruženým k profilu účtování. Každý záznam skupiny je specifický pro jednu hodnotu. Tuto hodnotu zadáte do pole, které se zobrazí za polem **Kód účtu**. Toto pole je obvykle pojmenováno **Účet** nebo **Číslo účtu/skupiny**. Přesný název se liší v závislosti na stránce, kde se vyskytuje.

Hodnota **Skupina** vyžaduje, abyste nejprve nakonfigurovali skupinu a propojili ji s jedním nebo více záznamy pro účet. Hodnota **Skupina** je méně konkrétní než hodnota **Tabulka**, ale konkrétnější než hodnota **Vše**. Pokud pro tabulku nebyl nakonfigurován žádný záznam, systém se pokusí najít záznam pro skupinu, do které záznam patří.

Pokud například pracujete s profilem odesílání zákazníků a vyberete možnost **Skupina** v poli **Kód účtu**, musíte vybrat skupinu zákazníků v poli **Číslo účtu/skupiny**. Musíte předdefinovat skupiny zákazníků na stránce **Skupina zákazníků** a při vytváření zákazníka musíte zadat skupinu zákazníků.

Pokud musíte pro daný typ účtování sledovat více hlavních účtů, doporučujeme použít hodnotu **Skupina**. Například máte tři hlavní obchodní účty pohledávek: jeden pro stálé zákazníky, jeden pro zaměstnance a jeden pro mezipodnikový prodej. V tomto případě doporučujeme vytvořit tři skupiny zákazníků pro segmentaci zákazníků. Poté namapujte každou skupinu zákazníků ke správnému hlavnímu účtu v profilu zákazníka. Následující tabulka ukazuje tři skupiny zákazníků pro tento příklad.

| Skupina odběratelů | Název | Popis |
|----------------|------|-------------|
| EXT | Externí odběratel | Tato skupina se používá pro všechny standardní externí zákazníky. |
| EMP | Zaměstnanci | Tato skupina se používá pro všechny zaměstnance, kteří nakupují ve vaší organizaci. |
| INT | Mezipodnikový prodej | Tato skupina se používá pro všechny mezipodnikové zákaznické účty, které se používají s integračními prodejními a nákupními objednávkami. |

V profilu účtování pak nastavíte tři řádky. Na každém řádku vyberete hodnotu **Skupina** a související hlavní účet.

### <a name="all-value"></a>Hodnota Vše

Hodnota **Vše** označuje, že nastavení platí pro všechny záznamy. Pokud vyberete hodnotu **Vše** v poli **Kód účtu**, pole **Číslo účtu/skupiny** není k dispozici a nemůžete vybrat konkrétní záznam, na který chcete konfiguraci použít.

Hodnota **Vše** je nejméně specifická hodnota. Používá se pouze v případě, že systém nemůže najít shodu pro hodnotu **Tabulka** nebo **Skupina**. Měli byste vybrat hodnotu **Vše**, když máte pouze jeden hlavní účet pro konkrétní typ účtování.

Když například pracujete s profilem účtování zákazníků, hlavní účty, které určíte, se vztahují na všechny ostatní zákazníky a skupiny zákazníků, které nemají záznam pro konkrétní tabulku (zákazník) nebo skupinu (skupina zákazníků).

### <a name="category"></a>Kategorie

Profily účtování zásob mají další hodnotu, která je specifická pro kategorii prodeje nebo kategorii nákupu. Tato hodnota se podobá hodnotě **Tabulka** v tom, že se vztahuje pouze na určitou kategorii prodeje nebo nákupu.

### <a name="default-value"></a>Výchozí hodnota

Pokud nevytvoříte záznam pro typ účtování v profilu účtování, kde je pole **Kód účtu** nastaveno na **Vše** a systém nemůže najít odpovídající záznam profilu účtování pro hodnotu **Skupina** nebo **Tabulka**, systém se vrátí na výchozí hodnotu, kterou lze zadat na stránce **Účty pro automatické transakce**. Více informací viz [Účty pro automatické transakce](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Clearingové účty

Termín *clearingový účet* se často používá v účetnictví. Některé typy účtování v aplikacích Microsoft Dynamics 365 jsou clearingové účty. Jinými slovy, zůstatek na účtu je vymazán nebo stornován při zaúčtování další transakce. Když například zaúčtujete příjemku produktu nákupní objednávky, součet odhadovaných nákladů na produkty plus daň a veškeré poplatky na řádcích nákupní objednávky se zaúčtují do typu účtování časového rozlišení nákupu jako závazek. Později, když fakturujete nákupní objednávku, se zůstatek stornuje z typu účtování časového rozlišení nákupu a přesune se na obchodní účet Závazky.

## <a name="additional-resources"></a>Další prostředky

Mnohé moduly v Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce a Dynamics 365 Project Operations mají profil účtování nebo další konfigurace, které řídí, jak funguje účtování do hlavní knihy. V následujících tématech se dozvíte více o profilech účtování a nastavení účtování v každém modulu:

- [Účty pro automatické transakce](accounts-for-auto-transactions.md)
- [Účtování závazků](accts-payble-posting.md)
- [Účtování pohledávek](accts-recvble-posting.md)
- [Účtování leasingu majetku](../asset-leasing/set-up-lease-posting-accts.md)
- Účtování správy majetku (již brzy)
- Účtování pokladny a banky (již brzy)
- Účty zaúčtování přecenění měny (již brzy)
- Účtování správy výdajů (již brzy)
- [Účetní profil dlouhodobého majetku](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Účtování mezipodnikového účetnictví (již brzy)
- Profil účtování zásob (již brzy)
- [Účtování nákladů s doručením](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Přehled definic účtování](posting-definitions.md)
- Účtování řízení výroby (již brzy)
- Účtování projektového řízení a účetnictví (již brzy)
- Účtování správy služeb (již brzy)
- Účtování daní (již brzy)
- Účtování času a účasti (již brzy)
- Účtování správy dopravy (již brzy)
- Profily zaúčtování správy rabatu (již brzy)
