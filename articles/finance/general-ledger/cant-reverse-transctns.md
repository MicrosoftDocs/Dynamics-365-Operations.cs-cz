---
title: Proč nemohu tuto transakci stornovat?
description: Toto téma popisuje různé důvody, proč transakce nelze stornovat. Uvádí také řešení tohoto problému.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 869832f085ee91f6c1fee53dad508cf5e54535627dadd6fb59a7586b03c8ec3b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719726"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Proč nemohu tuto transakci stornovat?

[!include [banner](../includes/banner.md)]

Toto téma popisuje různé důvody, proč transakce nelze stornovat. Uvádí také řešení tohoto problému.

## <a name="symptom"></a>Příznak

Organizace se mohou dostat do situací, kdy musí stornovat transakci, kterou zaúčtovaly. Systém jim příležitostně zabrání tyto transakce stornovat. Toto chování může vyvolat dvě otázky:

- Proč nemohu transakci stornovat?
- Jak funkce masového stornování ovlivňuje toto chování?

## <a name="resolution"></a>Řešení

Transakce musí před stornováním splňovat konkrétní kritéria. Zbývající části tohoto tématu poskytují ověření pro každý modul. Ačkoli se toto téma zaměřuje na transakce v Microsoft Dynamics 365 Finance, některé z konceptů a ověřování lze použít na jiné aplikace, jako například Dynamics 365 Supply Chain Management.

Místo, kde je transakce stornována, může navíc ovlivnit, zda ji lze stornovat. Například platbu dodavatele, která je zaúčtována jako šek, lze stornovat pouze ze sekce **Šeky** na stránce transakce pro bankovní účty. Nelze ji stornovat ze stránky **Transakce dokladu** v hlavní knize.

Pokud funkce **Hromadné stornování pro více dokumentů** (také známá jako funkce Hromadné stornování) je zapnutá v pracovním prostoru **Správa funkcí**, ovlivňuje to, kolik transakcí lze stornovat a kde je lze stornovat. Když je tato funkce zapnutá, poskytuje dvě výhody:

- U některých typů transakcí lze vybrat a stornovat více než jednu transakci z deníku, ze kterého byla zaúčtována, nebo ze stránky **Transakce dokladu**. Jednotlivé transakce však musely být před zapnutím funkce reverzibilní. Než byla tato funkce zavedena, transakce musely být stornovány po jedné.
- *Některé* transakce dílčí hlavní knihy lze stornovat z deníku (hlavního deníku) nebo ze stránky **Transakce dokladu**. Nemusí být stornovány ze stránky dílčí hlavní knihy. Například deník faktury dodavatele mohl být dříve stornován pouze ze stránky **Transakce dodavatele**. Nyní jej však lze stornovat také ze strany hlavní knihy, z deníku nebo ze stránky **Transakce dokladu**. Každá část tohoto tématu vysvětluje typy transakcí, na které se tato výhoda nevztahuje.

Funkce hromadného stornování **neumožňuje** stornování více typů transakcí. Pokud typ transakce nemohl být dříve stornován, nelze jej ani po zapnutí funkce stornovat. Faktury dodavatele nákupních objednávek například nelze stornovat bez ohledu na to, zda je zapnutá funkce hromadného stornování.

Další informace o funkci hromadného stornování naleznete v části [Stornování zaúčtování deníku](reverse-journal-posting.md).

## <a name="general-ledger"></a>Hlavní kniha

Úpravy hlavní knihy se zadávají pouze pomocí účtů hlavní knihy. Aktualizují proto pouze hlavní knihu.

Pokud je funkce hromadné stornování vypnuta, lze většinu úprav hlavní knihy jednotlivě stornovat ze stránky **Transakce pro \<main account\>** stránka pro hlavní knihu (**LedgerTransAccount**). (Přesný název stránky se liší v závislosti na vybraném hlavním účtu.) Stránka zobrazuje každou transakci, která byla zaúčtována na hlavní účet. Obvykle se otevírá ze stránky **Seznam předvah**, nebo výběrem **Transakce** na stránce **Transakce dokladu**.

Pokud je zapnuta funkce hromadného stornování, jeden nebo více dokladů hlavní knihy lze nyní stornovat ze stránky **Transakce dokladu** a z deníku, ze kterého byla transakce zaúčtována. Výjimkou jsou přecenění cizí měny v hlavní knize, konsolidace a transakce uzávěrky na konci roku. Tyto transakce jsou stornovány ze stránek, ze kterých bylo spuštěno uzavření konce roku.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Důvody, proč transakce nelze stornovat

Transakce nelze stornovat z následujících důvodů:

- Hlavní deník:

    - Fiskální období je pozastaveno nebo trvale uzavřeno:

        - Pokud je datum stornování ve fiskálním období, které není otevřené, transakci nelze stornovat.
        - Pokud transakce podporuje zadání data stornování, transakci lze stále stornovat změnou data stornování na otevřené období.

    - Byl spuštěn proces uzavření na konci roku:

        - Účetní datum transakce je ve fiskálním roce, který prošel uzávěrkou na konci roku. Ačkoli období ve fiskálním roce může být stále otevřené, transakci nelze stornovat, pokud byl pro fiskální rok spuštěn proces uzavření konce roku. Fiskální rok má jiný status než období v něm.
        - Uzavření konce roku lze stornovat a poté lze transakci stornovat. Tento přístup nemusí být ideální volbou. V závislosti na stavu procesu fiskální uzávěrky může být jednodušší ručně zadat stronovací transakci v otevřeném období buď uzavřeného fiskálního roku, nebo příštího fiskálního roku. Pokud je nová transakce zaúčtována do otevřeného období fiskálního roku, který prošel procesem uzavření konce roku, uzavření konce roku musí být spuštěno znovu.

    - Stornování transakce již probíhá:

        - Pokud se transakce právě stornuje, musí být tento proces dokončen. Nelze provést samostatný proces stornování. 
        - Poté, co je stornování dokončeno, lze stornovanou transakci stornovat znovu (tj. lze stornovat storno).

    - Vyrovnání hlavní knihy:

        - Pokud byl jeden nebo více řádků transakce vypořádán účetní knihou pomocí periodického úkolu **Vyrovnání hlavní knihy** (**Hlavní kniha \> Periodické úkoly \> Vyrovnání hlavní knihy**), takže existuje záznam v tabulce LedgerTransSettlement, transakci nelze stornovat.
        - Vyrovnání deníku lze stornovat a poté lze doklad stornovat.

    - Mezipodnikové:

        - Pokud je transakce mezipodnikovou transakcí, nelze ji stornovat.
        - Transakce **není** mezipodniková transakce, ale je zaúčtována na hlavní účet „splatný do“ nebo „splatný od“, který byl definován na stránce **Mezipodnikové nastavení**.

    - Časové rozlišení:

        - Pokud je stornován časově rozlišený doklad hlavní knihy, časově rozlišený záznam a všechny odpovídající dílčí transakce časového rozlišení budou stornovány.
        - Jednotlivé dílčí transakce časového rozlišení nelze stornovat.

- Deník uznání výnosů:

    - Transakce uznání výnosů nelze stornovat.
    - Když jsou výnosy uznány prostřednictvím deníku rozpoznávání výnosů, doklad je zaúčtován pouze na účty hlavní knihy. Proto na stránkách jako **Transakce dokladu** transakce vypadají, jako by se jednalo pouze o položky hlavní knihy.

- Přecenění cizí měny:

    - Transakce přecenění cizí měny lze stornovat, ale pouze ze stránky **Přecenění cizí měny** hlavní knihy, ze které bylo provedeno přecenění.
    - Stornování lze provést pouze v případě, že je zaúčtováno do otevřeného fiskálního období.

- Konsolidace:

    - Konsolidační transakce lze stornovat, ale pouze ze stránky **Konsolidační transakce**.
    - Stornování lze provést pouze v případě, že je zaúčtováno do otevřeného fiskálního období.

- Roční uzávěrka:

    - Transakcí uzávěrky na konci roku (uzavírací i otevírací transakce) lze stornovat těmito způsoby:

        - Pokud je funkce vylepšení uzávěrky na konci roku hlavní knihy vypnutá, vyberte možnost **Vrátit předchozí uzávěrky** v dialogovém okně **Uzávěrka na konci roku**.
        - Pokud je zapnuta funkce vylepšení uzávěrky na konci roku hlavní knihy, vyberte záznamy o společnosti a fiskálním roce, které byly vytvořeny pro uzavření konce roku na stránce **Uzávěrka na konci roku** a poté vyberte **Stornovat uzávěrku na konci roku**.

    - Všimněte si, že stornování uzávěrky konce roku ve skutečnosti odstraní uzavírací a otevírací transakce. Nikdy není zaúčtován stornující doklad.

## <a name="accounts-payable"></a>Závazky

Několik typů transakcí aktualizuje dílčí hlavní knihu závazků. Mezi příklady patří faktury dodavatele, deníky faktur dodavatelů a výkazy výdajů.

Pokud je funkce hromadného stornování vypnuta, transakce lze stornovat jednotlivě buď ze stránky **Transakce dodavatele** pro faktury nebo na stránce **Bankovní účet** pro platby šekem.

Pokud je zapnuta funkce hromadného stornování, jednu nebo více transakcí závazků lze též stornovat ze stránky **Transakce dokladu** a z deníku, ze kterého byly transakce zaúčtovány. Platby dodavatele však lze i nadále stornovat pouze z bankovního účtu. Navíc transakce dodavatele nelze stornovat ze stránky **Transakce pro \<main account\>** pro hlavní knihu. Lze je stornovat pouze ze stránky **Transakce dokladu**.

Některé transakce nelze vůbec stornovat. Mezi příklady patří faktury dodavatele nákupní objednávky a elektronické platby dodavatele.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Důvody, proč doklady nelze stornovat

Doklady nelze stornovat z následujících důvodů:

- Fiskální období je pozastaveno nebo uzavřeno:

    - Pokud je datum stornování ve fiskálním období, které není otevřené, transakci nelze stornovat.
    - Pokud transakce podporuje zadání data stornování, transakci lze stále stornovat změnou data stornování na otevřené období.

- Byl spuštěn proces uzavření na konci roku hlavní knihy:

    - Účetní datum transakce je ve fiskálním roce, který byl uzavřen v hlavní knize. Ačkoli období ve fiskálním roce může být stále otevřené, transakci nelze stornovat, pokud byl pro fiskální rok spuštěn proces uzavření konce roku. Fiskální rok má jiný status než období v něm.
    - Uzavření konce roku lze stornovat a poté lze transakci stornovat. Tento přístup nemusí být ideální volbou. V závislosti na stavu procesu fiskální uzávěrky může být jednodušší ručně zadat stronovací transakci v otevřeném období buď uzavřeného fiskálního roku, nebo příštího fiskálního roku. Pokud je nová transakce zaúčtována do otevřeného období fiskálního roku, který prošel procesem uzavření konce roku, uzavření konce roku musí být spuštěno znovu.

- Položka dílčí hlavní knihy nebyla přenesena do hlavní knihy:

    - Tento důvod se vztahuje pouze na jiné než faktury dodavatele nákupní objednávky.
    - Použijte stránku **Položky dílčí hlavní knihy, které ještě nebyly přeneseny** pro přenos záznamu do hlavní knihy. Jiné než faktury dodavatele nnákupní objednávky lze poté stornovat ze stránky **Transakce dodavatele**.

- Vyrovnání:

    - Transakce (například faktura nebo platba) je vypořádána nebo označena k vypořádání.

        - Můžete ověřit, zda je transakce vypořádána nebo označena k vypořádání výběrem **Zobrazit vyrovnání** nebo **Vyrovnání \> Historie vyrovnání** na stránce **Transakce dodavatele**.
        - Vypořádání můžete také stornovat ze stránky **Transakce dodavatele** (**Vyrovnání \> Zrušit vyrovnání**), pokud musí být jedna z transakcí stornována.

- Doklad obsahuje více než jednu transakci dílčí hlavní knihy, která byla zadána pomocí stejného čísla dokladu (vydání jednoho dokladu).
- Faktura nebyla schválena:

    - Pokud na faktuře není zaškrtnuto políčko **Schválení**, fakturu nelze stornovat.

        - V tomto případě schválení neodkazuje na schválení v procesu pracovního postupu, ale na možnost **Schválení** na faktuře. Tato možnost slouží k zabránění zaplacení faktury. Obvykle se používá pro faktury registrované dodavatelem.

- Transakce je ve fondu faktur:

    - Fakturu ve fondu nelze stornovat přímo ze stránky **Transakce dodavatele**. Místo toho musí být stornována procesem zrušení na stránce **Deník schválení faktur**.

- Transakce má nadřízenou fakturu, která byla opravena (indická lokalizace).
- Transakce má stav **Uhrazená faktura**.
- Transakce slouží k částečnému vyrovnání daně.
- Transakce obsahuje účet dodavatele, ale stornuje se z nesprávné stránky, například ze sránky **Transakce pro \<main account\>**:

    - Jak naznačuje tento důvod, i když je zapnutá funkce hromadného stornování, některé transakce dílčí hlavní knihy lze stornovat pouze z konkrétních stránek.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typy transakcí, které nelze stornovat

Následující typy transakcí nelze stornovat:

- Přecenění cizí měny:

    - Na rozdíl od přecenění cizí měny hlavní knihy nelze stornovat přecenění cizí měny závazků a pohledávek. Místo toho musí být přecenění spuštěno znovu pomocí data faktury. V tomto případě přecenění použije směnný kurz k datu faktury a v podstatě převede nerealizovaný zisk nebo ztrátu na 0 (nula). Výsledek se tedy podobá výsledku stornování předchozího přecenění. Pamatujte však, že stejná částka nebude stornována, pokud byl na faktuře změněn výchozí směnný kurz.

- Faktura dodavatele nákupní objednávky:

    - Ke stornování faktury dodavatele je nutné vytvořit dobropis. Další informace o tom, jak vytvořit stornující transakci, najdete v tématu [Vytvoření nákupní vratky](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Vlastní směnka
- Dodávka exportu akreditivu banky

## <a name="accounts-receivable"></a>Pohledávky

Několik typů transakcí aktualizuje dílčí hlavní knihu pohledávek. Mezi příklady patří zákaznické faktury z prodejních objednávek, zákaznické faktury zadávané prostřednictvím obecného deníku, faktury s volným textem, platby odběratelům a odpisy.

Pokud je funkce hromadného stornování vypnuta, transakce lze stornovat jednotlivě buď ze stránky **Transakce odběratele** pro faktury nebo na stránce **Bankovní účty** pro vklady. Informace o zrušení platby naleznete v části [Správa hotovosti a banky](cant-reverse-transctns.md#cash-and-bank-management) dále v tomto tématu.

Pokud je zapnuta funkce hromadného stornování, jednu nebo více transakcí pohledávek lze též stornovat ze stránky **Transakce dokladu** a z deníku, ze kterého byly transakce zaúčtovány. Vklady však lze i nadále stornovat pouze z bankovního účtu a faktury s volným textem lze stornovat pouze z původní stránky (pokud je zapnutá funkce umožňující opravy). Navíc transakce odběratele nelze stále stornovat ze stránky **Transakce pro \<main account\>** pro hlavní knihu. Lze je však stornovat ze stránky **Transakce dokladu**.

Některé transakce nelze stornovat. Mezi příklady patří faktury a odpisy prodejních objednávek odběratelů.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Důvody, proč transakce nelze stornovat

Transakce nelze stornovat z následujících důvodů:

- Fiskální období je pozastaveno nebo trvale uzavřeno:

    - Pokud je datum stornování ve fiskálním období, které není otevřené, transakci nelze stornovat.
    - Pokud transakce podporuje zadání data stornování, transakci lze stále stornovat změnou data stornování na otevřené období.

- Byl spuštěn proces uzavření na konci roku hlavní knihy:

    - Účetní datum transakce je ve fiskálním roce, který prošel uzávěrkou hlavní knihy na konci roku. Ačkoli období ve fiskálním roce může být stále otevřené, transakci nelze stornovat, pokud byl pro fiskální rok spuštěn proces uzavření konce roku. Fiskální rok má jiný status než období v něm.
    - Uzavření konce roku lze stornovat a poté lze transakci stornovat. Tento přístup nemusí být ideální volbou. V závislosti na stavu procesu fiskální uzávěrky může být jednodušší ručně zadat stronovací transakci v otevřeném období buď uzavřeného fiskálního roku, nebo příštího fiskálního roku. Pokud je nová transakce zaúčtována do otevřeného období fiskálního roku, který prošel procesem uzavření konce roku, uzavření konce roku musí být spuštěno znovu.

- Položka dílčí hlavní knihy nebyla přenesena do hlavní knihy:

    - Tento důvod se týká pouze bezplatných textových faktur.
    - Použijte stránku **Položky dílčí hlavní knihy, které ještě nebyly přeneseny** pro přenos záznamu do hlavní knihy. Fakturu s volným textem lze poté zrušit nebo opravit, pokud je povolena funkce oprav.

- Vyrovnání:

    - Transakce (například faktura nebo platba) je vypořádána nebo označena k vypořádání.

        - Můžete ověřit, zda je transakce vypořádána nebo označena k vypořádání výběrem **Zobrazit vyrovnání** nebo **Vyrovnání \> Historie vyrovnání** na stránce **Transakce odběratele**.
        - Vypořádání můžete také stornovat ze stránky **Transakce odběratele** (**Vyrovnání \> Zrušit vyrovnání**), pokud musí být jedna z transakcí stornována.

- Transakce obsahuje více než jednu transakci dílčí hlavní knihy, která byla zadána pomocí stejného čísla dokladu (vydání jednoho dokladu).
- Faktura nebyla schválena:

    - Pokud na faktuře není zaškrtnuto políčko **Schválení**, fakturu nelze stornovat.

        - V tomto případě schválení neodkazuje na schválení v procesu pracovního postupu, ale na možnost **Schválení** na řádcích dokladu. Tato možnost slouží k zabránění zaplacení faktury. Ačkoli se tato možnost obvykle používá u závazků, je k dispozici také pro faktury za pohledávky, které se zadávají prostřednictvím deníků.

- Transakce má nadřízenou fakturu, která byla opravena (indická lokalizace).
- Transakce obsahuje účet odběratele, ale stornuje se z nesprávné stránky, například ze sránky **Transakce pro \<main account\>**:

    - Jak naznačuje tento důvod, i když je zapnutá funkce hromadného stornování, některé transakce dílčí hlavní knihy lze stornovat pouze z konkrétních stránek.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typy transakcí, které nelze stornovat

Následující typy transakcí nelze stornovat:

- Přecenění cizí měny:

    - Na rozdíl od přecenění cizí měny hlavní knihy nelze stornovat přecenění cizí měny závazků a pohledávek. Místo toho musí být přecenění spuštěno znovu pomocí data faktury. V tomto případě přecenění použije směnný kurz k datu faktury a v podstatě převede nerealizovaný zisk nebo ztrátu na 0 (nula). Výsledek se tedy podobá výsledku stornování předchozího přecenění. Pamatujte však, že stejná částka nebude stornována, pokud byl na faktuře změněn výchozí směnný kurz.

- Transakce, která upravila srážku daně
- Faktura odběratele za prodejní objednávku:

    - Ke stornování transakce nutné vytvořit dobropis nebo vratku. Informace o tom, jak vytvořit reverzní transakci, najdete v tématu [Vratky prodeje](../../supply-chain/warehousing/sales-returns.md).

- Cizí směnka
- Pokladní transakce
- Rozšířené vyrovnání
- Oznámení úroků
- Upomínka
- Bankovní akreditiv
- Exportní dodávka
- Deník uznání výnosů:

    - Když jsou výnosy uznány prostřednictvím deníku rozpoznávání výnosů, doklady jsou zaúčtovány na účty hlavní knihy. Proto se zdají, jako by to byly pouze položky hlavní knihy. Tyto položky nelze stornovat, protože plán výnosů nebude znovu otevřen, aby bylo možné tržby znovu rozpoznat.

## <a name="cash-and-bank-management"></a>Pokladna a banka

Několik typů transakcí aktualizuje dílčí hlavní knihu banky prostřednictvím obecného deníku. Mezi příklady patří platby dodavatelům, platby zákazníkům a bankovní převody.

Pokud je funkce hromadného stornování vypnuta, transakce lze stornovat jednotlivě buď ze stránky **Bankovní účty** pro šeky a vklady nebo na stránce **Transakce odběratele** pro platby odběratele.

Pokud je zapnuta funkce hromadného stornování, jednu nebo více platebních transakcí lze též stornovat ze stránky **Transakce dokladu** a z deníku, ze kterého byly transakce zaúčtovány. Vklady však lze i nadále stornovat pouze z bankovního účtu. Navíc bankovní transakce nelze stále stornovat ze stránky **Transakce pro \<main account\>** hlavní knihy. Lze je však stornovat ze stránky **Transakce dokladu**.

Některé transakce nelze stornovat. Mezi příklady patří elektronické platby dodavatele.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Důvody, proč transakce nelze stornovat

Transakce nelze stornovat z následujících důvodů:

- Fiskální období je pozastaveno nebo trvale uzavřeno:

    - Pokud je datum stornování ve fiskálním období, které není otevřené, transakci nelze stornovat.
    - Pokud transakce podporuje zadání data stornování, transakci lze stále stornovat změnou data stornování na otevřené období.

- Byl spuštěn proces uzavření na konci roku hlavní knihy:

    - Účetní datum transakce je ve fiskálním roce, který prošel uzávěrkou hlavní knihy na konci roku. Ačkoli období ve fiskálním roce může být stále otevřené, transakci nelze stornovat, pokud byl pro fiskální rok spuštěn proces uzavření konce roku. Fiskální rok má jiný status než období v něm.
    - Uzavření konce roku lze stornovat a poté lze transakci stornovat. Tento přístup nemusí být ideální volbou. V závislosti na stavu procesu fiskální uzávěrky může být jednodušší ručně zadat stronovací transakci v otevřeném období buď uzavřeného fiskálního roku, nebo příštího fiskálního roku. Pokud je nová transakce zaúčtována do otevřeného období fiskálního roku, který prošel procesem uzavření konce roku, uzavření konce roku musí být spuštěno znovu.

- Vyrovnání:

    - Transakce (platba) je vypořádána nebo označena k vypořádání.

        - Můžete ověřit, zda je transakce vypořádána nebo označena k vypořádání výběrem **Zobrazit vyrovnání** nebo **Vyrovnání \> Historie vyrovnání** na stránce **Transakce odběratele** nebo **Transkace odběratele**.
        - Vypořádání můžete také stornovat ze stránky **Transakce dodavatele** nebo **Transakce odběratele** (**Vyrovnání \> Zrušit vyrovnání**), pokud musí být jedna z transakcí stornována.

- Transakce obsahuje více než jednu transakci dílčí hlavní knihy, která byla zadána pomocí stejného čísla dokladu (vydání jednoho dokladu).
- Překlenovací transakce:

    - Pokud transakce souvisí s překlenovací platbou, nelze ji stornovat.
    - Pokud je nutné překlenovací platbu vrátit, musí být platba nejprve zúčtována z překlenovacího účtu do banky. Platbu pak lze stornovat za předpokladu, že splňuje další ověřovací kritéria.

- Transakce obsahuje bankovní účet, ale je stornována na stránce **Transakce pro \<main account\>** nebo z nesprávné dílčí účetní knihy, jako jsou pohledávky nebo závazky:

    - Jak naznačuje tento důvod, i když je zapnutá funkce hromadného stornování, některé transakce dílčí hlavní knihy lze stornovat pouze z konkrétních stránek.

- Banka - přecenění cizí měny:

    - Přecenění cizí měny banky lze stornovat. Stornu však lze zabránit, pokud provedete kroky storna mimo chronologické pořadí. Pokud jste například provedli přecenění v březnu a dubnu, březnové přecenění nelze vrátit, dokud není zrušeno dubnové přecenění.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typy transakcí, které nelze stornovat

Následující typy transakcí nelze stornovat:

- Platby dodavatele, které byly provedeny jako elektronické převody prostředků (EFT)
- Vlastní směnky
- Cizí směnky

## <a name="fixed-assets"></a>Dlouhodobý majetek

Několik typů transakcí aktualizuje dílčí účetní knihu Dlouhodobý majetek. Mezi příklady patří akvizice a odpisy.

Pokud je funkce Hromadné storno vypnuta, transakce lze stornovat jednotlivě na stránce **Transakce dodavatele**, na stránce **Transakce dlouhodobého majetku** nebo z leasingu majetku, v závislosti na typu transakce.

Pokud je zapnuta funkce hromadného stornování, jednu nebo více transakcí dlouhodobého majetku lze též stornovat ze stránky **Transakce dokladu** v deníku, ze kterého byly transakce zaúčtovány.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Důvody, proč transakce nelze stornovat

Transakce nelze stornovat z následujících důvodů:

- Fiskální období je pozastaveno nebo trvale uzavřeno:

    - Pokud je datum stornování ve fiskálním období, které není otevřené, transakci nelze stornovat.
    - Pokud transakce podporuje zadání data stornování, transakci lze stále stornovat změnou data stornování na otevřené období.

- Byl spuštěn proces uzavření na konci roku hlavní knihy:

    - Účetní datum transakce je ve fiskálním roce, který byl uzavřen v hlavní knize. Ačkoli období ve fiskálním roce může být stále otevřené, transakci nelze stornovat, pokud byl pro fiskální rok spuštěn proces uzavření konce roku. Fiskální rok má jiný status než období v něm.
    - Uzavření konce roku lze stornovat a poté lze transakci stornovat. Tento přístup nemusí být ideální volbou. V závislosti na stavu procesu fiskální uzávěrky může být jednodušší ručně zadat stronovací transakci v otevřeném období buď uzavřeného fiskálního roku, nebo příštího fiskálního roku. Pokud je nová transakce zaúčtována do otevřeného období fiskálního roku, který prošel procesem uzavření konce roku, uzavření konce roku musí být spuštěno znovu.

- Akvizice:

    - Pokud k akvizici došlo na faktuře dodavatele nákupní objednávky, musí být storno provedeno zadáním dobropisu dodavatele. Informace o tom, jak vložit stornující transakci, najdete v tématu [Vytvoření nákupní vratky](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - K akvizici došlo při transakci projektu.
    - Akvizici nelze stornovat poté, co jsou u majetku zaúčtovány odpisy. Aby bylo možné akvizici stornovat, musí být odpisy zrušeny.
    - Pokud stav hodnotového modelu nebo odpisové knihy pro dlouhodobý majetek není otevřený, transakci nelze stornovat.

- Vyřazení:

    - Vyřazení se provádí prostřednictvím faktury s volným textem:

        - Oprava faktury s volným textem je blokována, pokud obsahuje dlouhodobý majetek. Pokud je však majetek vyřazen prostřednictvím deníku, lze fakturu s volným textem stornovat ze záznamu dlouhodobého majetku.

    - Pokud stav hodnotového modelu nebo odpisové knihy pro dlouhodobý majetek není otevřený, transakci nelze stornovat.

- Odpisy:

    - Odpisy **lze** stornovat, pokud jsou zaúčtovány také následné odpisy. Obdržíte však varování, protože tento přístup není osvědčeným postupem.
    - Pokud stav hodnotového modelu nebo odpisové knihy pro dlouhodobý majetek není otevřený, transakci nelze stornovat.

- Transakce (nebo reverzní transakce) pro konkrétní aktiva a knihu aktiv existují pro datum transakce dokladu nebo později.
- Transakce obsahuje majetkový účet, ale je stornována na stránce **Transakce pro \<main account\>** nebo z nesprávné dílčí účetní knihy, jako jsou pohledávky nebo závazky:

    - Jak naznačuje tento důvod, i když je zapnutá funkce hromadného stornování, některé transakce dílčí hlavní knihy lze stornovat pouze z konkrétních stránek.
    - Pokud k akvizici dojde na faktuře dodavatele, která není nákupní objednávkou, nebo v deníku faktur dodavatele, lze ji stornovat pouze na stránce **Transakce prodejce** v závazcích.
    - Pokud je majetek získán z leasingu majetku, lze jej stornovat na stránce **Transakce pasiv** v leasingu majetku.
