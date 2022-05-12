---
title: Parametry zaúčtování Commerce
description: Toto téma popisuje parametry, které jsou specifické pro účtování finančních a fyzických transakcí v Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649193"
---
# <a name="commerce-posting-parameters"></a>Parametry zaúčtování Commerce

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje parametry, které jsou specifické pro účtování finančních a fyzických transakcí v Microsoft Dynamics 365 Commerce. Parametry zaúčtování Commerce se nacházejí v centrále Commerce v nabídce **Maloobchod a obchod \> Nastavení centrály \> Parametry \> Parametry Commerce \> Zaúčtování**.

## <a name="periodic-discount-parameters"></a>Parametr časové slevy

Následující tabulka uvádí parametry časové slevy, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Zaúčtovat časovou slevu | Tato možnost řídí, zda jsou časové nabídky účtovány do účtů hlavní knihy. Mezi časové slevy patří kombinační slevy, slevy, množstevní slevy a zlevněné nabídky. Když je tento parametr povolen, lze další pole nastavit v části **Časové slevy**. |
| Typ účtu hlavní knihy | <p>Vyberte typ účtu používaný pro zaúčtování časových slev.</p><ul><li>**Standardní** – Systém na této stránce nepoužívá pole související se slevou. Místo toho používá účty, které jsou definovány na stránce **Zaúčtování** v centrále Commerce (**Řízení zásob \> Nastavení \> Zaúčtování \> Formuláře zaúčtování**).</li><li>**Pravidelné** – Systém používá slevové účty Commerce, které jsou určeny v polích souvisejících se slevou na této stránce. Pokud vyberete tuto možnost, musíte zadat účet hlavní knihy (HK) pro každý typ nabídky (sleva, kombinační sleva, množství, prahová hodnota). Při nastavování každé slevy můžete definovat účet. Při použití funkce účtování do slevového účtu na stránce nastavení slevy se provede další debetní a kreditní položka, aby se zaúčtování slevy překlasifikovalo z účtu HK slevy Commerce na účet HK slevy. Více informací získáte v části [Maloobchodní slevy](retail-discounts-overview.md).</li></ul> |
| Zaúčtovat slevu za infokód | Tato možnost se již ve standardním řešení Commerce nepoužívá a bude označena jako zastaralá. |
| Zaúčtovat časovou slevu pro objednávky | Tato možnost kontroluje, zda maloobchodní časové slevy budou zaúčtovány do hlavní knihy pro objednávku zákazníka a objednávky v kontaktním středisku. |

## <a name="inventory-update-parameters"></a>Parametry aktualizace zásob

Následující tabulka uvádí parametry aktualizace zásob, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Použít výchozí ID dávky, když nejsou nalezena čísla dávky | Tato možnost řídí, zda se použije výchozí ID dávky u položek s povoleným dávkovým zpracováním, když čísla dávky pro položky nejsou nalezena a pro tyto položky jsou povoleny záporné zásoby. |
| Výchozí ID dávky | Číslo dávky, které se použije, když čísla dávky pro položky nejsou nalezena a je zapnutý parametr **Použít výchozí ID dávky, když nejsou nalezena čísla dávky**. |

## <a name="aggregation-parameters"></a>Parametry agregace

Následující tabulka uvádí parametry agregace, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Odvod do trezoru | Povolte tento parametr, chcete-li agregovat všechny transakce během zaúčtování výpisu a vytvořit jeden řádek v deníku pro zaúčtování namísto samostatného řádku pro každý odvod. |
| Odvod do banky | Povolte tento parametr, chcete-li agregovat všechny transakce během zaúčtování výpisu a vytvořit jeden řádek v deníku pro zaúčtování namísto samostatného řádku pro každý odvod. |
| Prodejní transakce | Povolte tento parametr, chcete-li konsolidovat transakce jako součást procesu zaúčtování výpisu transakce. Doporučujeme, abyste tento parametr zapnuli. Dříve se jmenoval **Transakce dokladu**. |
| Neagregovat vrácení | Pokud je vybrána tato možnost, každá transakce vrácení bude zaúčtována jako samostatná prodejní objednávka při zaúčtování maloobchodního výkazu. |

## <a name="batch-processing-parameters"></a>Parametry dávkového zpracování

Následující tabulka uvádí parametry dávkového zpracování, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Maximální počet paralelních výkazů | Toto pole definuje počet dávkových úloh, které se používají k zaúčtování více výkazů. |
| Max. počet vláken pro zpracování objednávky na jeden výkaz | Toto pole představuje maximální počet vláken, které používá dávková úloha zaúčtování výkazu k vytvoření a fakturaci prodejních objednávek pro jeden výkaz. Celkový počet vláken, která používá proces zaúčtování výkazu, se vypočítá vynásobením hodnoty v tomto parametru hodnotou parametru **Maximální počet zaúčtování paralelních příkazů**. Nastavení příliš vysoké hodnoty tohoto parametru může negativně ovlivnit výkon procesu zaúčtování výkazu. |
| Max. počet řádků transakcí v rámci agregace | Toto pole definuje počet řádků transakce, které budou zahrnuty do jedné agregované transakce před vytvořením nové. Agregované transakce jsou vytvářeny na základě různých agregačních kritérií, jako je například odběratel, obchodní datum nebo finanční dimenze. Poznámka: řádky z jedné transakce nebudou rozděleny mezi různé agregované transakce. Proto počet řádků v agregované transakci může být o něco vyšší nebo nižší podle různých faktorů, jako je například počet různých produktů. |
| Maximální počet vláken pro ověření transakcí obchodu | Toto pole definuje maximální počet vláken, které lze použít pro ověření transakcí. Ověření transakcí je povinný krok, ke kterému musí dojít předtím, než mohou být transakce načteny do výkazů. Musíte rovněž definovat produkt dárkového poukazu na pevné záložce **Dárkový poukaz** na kartě **Zaúčtování** stránky **Parametry Commerce**, pokud organizace nepoužívá dárkové poukazy. |

V následující tabulce jsou uvedeny doporučené hodnoty pro parametry z předchozí tabulky. Tyto hodnoty by měly být otestovány a přizpůsobeny konfiguraci nasazení a dostupné infrastruktuře. Hodnoty převyšující doporučené hodnoty mohou nepříznivě ovlivnit jiné dávkové zpracování a měly by být ověřeny.

| Parametr | Doporučená hodnota | Podrobnosti |
|-----------|-------------------|---------|
| Maximální počet zaúčtování paralelních příkazů | <p>Nastavte tento parametr na počet dávkových úloh, které jsou dostupné pro skupinu dávek, která provádí úlohu **Výpis**.</p><p>**Obecné pravidlo:** Vynásobte počet virtuálních serverů AOS počtem dávkových úloh, které jsou k dispozici na virtuálním serveru AOS.</p> | Tento parametr nelze použít, když je povolena funkce **Výkazy maloobchodu – Postupné**. |
| Max. počet vláken pro zpracování objednávky na jeden výkaz | Začněte testovat hodnoty od **4**. Obvykle by tato hodnota neměla překročit **8**. | Tento parametr definuje počet vláken, která se používají k vytvoření a zaúčtování prodejních objednávek. Představuje počet vláken, která jsou k dispozici pro zaúčtování na jeden výpis. |
| Max. počet řádků transakcí v rámci agregace | Začněte testovat hodnoty od **1000**. V závislosti na konfiguraci centrály Commerce mohou být z hlediska výkonu výhodnější menší objednávky. | Tento parametr definuje počet řádků, které jsou zahrnuty do každé prodejní objednávky během účtování výkazu. Po dosažení tohoto počtu budou řádky rozděleny do nové objednávky. Počet prodejních řádků nebude stejný jako nastavený počet, protože k rozdělení dochází na úrovni prodejní objednávky. Číslo se však bude blížit nastavenému číslu. Tento parametr se používá ke generování prodejních objednávek pro maloobchodní transakce, které nemají pojmenovaného zákazníka. |
| Maximální počet vláken pro ověření transakcí obchodu | Doporučujeme nastavit tento parametr na **4** a zvýšit ho pouze v případě, že nedosáhnete přijatelného výkonu. Počet vláken, která tento proces používá, nemůže překročit počet procesorů, které jsou dostupné pro dávkový server. Pokud je počet vláken příliš vysoký, může být ovlivněno jiné dávkové zpracování. | Tento parametr řídí počet transakcí, které lze pro daný obchod současně ověřit. |

> [!NOTE]
> Všechna nastavení a parametry související se zaúčtováním výkazu, které jsou definovány v obchodech a na stránce **Parametry Commerce**, se vztahují na vylepšenou funkci zaúčtování výkazu.

## <a name="invoice-parameters"></a>Parametry faktury

Následující tabulka uvádí parametry faktury, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Název deníku | Název deníku plateb, který se používá při vytváření deníků plateb zákazníka pro platby prodejní objednávky. Toto nastavení se vztahuje na všechny platby za objednávky, které jsou zaúčtovány pro objednávky v pokladním místě (POS), kontaktním středisku a kanálu e-commerce. |
| Název účtu | Název platebního účtu. |
| Dát prioritu dimenzím z platební metody | Pokud je příznak povolen, bude deník plateb prioritizovat dimenze z platební metody namísto dimenzí z obchodu. |
| Chování výpočtu daně | Tento parametr určuje chování, když jsou fakturovány prodejní objednávky vytvořené během účtování výkazu:<ul><li>**Přepočítat** – Znovu vypočítat daně.</li><li> **Nepřepočítat** – Použijí se částky daně, které jsou vypočteny v pokladním místě.</li></ul> |
| Název deníku | Název deníku, který se používá při vytváření deníku plateb zákazníka pro vratky. Toto nastavení se vztahuje na všechny platby za objednávky, které jsou zaúčtovány pro objednávky v pokladním místě (POS), kontaktním středisku a kanálu e-commerce. |

## <a name="statement-parameters"></a>Parametry výkazu

Následující tabulka uvádí parametry výkazu, které jsou specifické pro účtování finančních a fyzických transakcí.

| Parametr | Popis |
|-----------|-------------|
| Rezervovat zásoby během výpočtu | Když je tento parametr povolen, výpočet výkazu dočasně rezervuje zásoby, dokud není výkaz zaúčtován. Tento parametr je ve výchozím nastavení zakázán, aby pomohl zlepšit výkon výpočtu výkazů. Aktualizované informace o zásobách lze vypočítat pomocí dávkové úlohy **Zaúčtovat zásoby**. Poznámka: dávková úloha zásob **Zaúčtovat** se již nepoužívá, když je povoleno vytváření objednávek [s postupným účtováním](trickle-feed.md) u maloobchodních transakcí. |
| Je vyžadována deaktivace inventur | Tento příznak deaktivuje inventuru během zaúčtování na centrále Commerce. |
| Při chybě znovu vypočítat finanční dimenze | Když je tento parametr povolen, u následujících zaúčtování výkazů dojde k opětovnému vypočítání finanční dimenze, pokud selže zaúčtování výkazu. |
| Použít finanční dimenze z obchodu vratky | Když je tento parametr povolen, lze vytvořit propojená vrácení prodejní objednávky, která používají finanční dimenze obchodu namísto finančních dimenzí z původní transakce. |
| Zrušit propojení vrácení | Když je tento parametr povolen, může výkaz vytvářet vrácení nezaúčtovaných prodejů jako slepá vrácení. Tento parametr je ve výchozím nastavení zakázán a doporučujeme jej tak ponechat. |
| Zakázat zaúčtování haléřových rozdílů | Tento parametr zakáže zaúčtování haléřových rozdílů mezi platbou transakce a hrubou částkou během zpracování plateb. |
| Automatické vyrovnání vkladů zákazníků | Když je tento parametr povolen, vklady zákazníků zaúčtované během zpracování výkazu maloobchodu jsou vyrovnány s otevřenými transakcemi zákazníka. |
| Povolení a používání odsouhlasení řízení hotovosti z pokladního místa | Když je tento parametr povolen, provádí se odsouhlasení řízení hotovosti v pokladním místě a hodnoty jsou předány do maloobchodního účetního výkazu, aby se vytvořily řádky výkazu. |
| Úroveň podrobností dokladu knihy | Tento parametr definuje úroveň podrobností, která je zahrnuta v dokladu hlavní knihy pro vybrané transakce, které pocházejí z pokladního místa. Typy transakcí zahrnují výnosy, výdaje a slevy. U slev je tento parametr zohledněn pouze v případě, že číslo účtu pro časovou slevu a číslo účtu pro pravidelnou slevu nejsou stejné. Pokud nejsou vyžadovány podrobnosti, je pro tato zaúčtování doporučenou hodnotou **Souhrn**. Když je definováno zaúčtování na úrovni souhrnu, nebude vyplněna hodnota **TransactionDiscountTrans.RecID**. Ve verzi Commerce 10.0.27 byl tento příznak přejmenován a přesunut. Dříve se jmenoval **Úroveň detailů** a byl v části **Aktualizace zásob**. |
