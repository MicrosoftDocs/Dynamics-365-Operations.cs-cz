---
title: Přidělení vlny
description: Toto téma popisuje, jak vytvořit krok přidělení vlny, včetně toho, jak pro něj povolit paralelní zpracování.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b01de3c9f1cbcb24abc2b5a0c91db7f0791020bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018996"
---
# <a name="wave-allocation"></a>Přidělení vlny

[!include [banner](../includes/banner.md)]

Zpracování vlny může být časově náročné a většina času zpracování je věnována kroku přidělení a kroku vytvoření práce.

Nyní je možné spustit každý z těchto kroků paralelně, což může zlepšit výkon zpracování vln a umožnit větší propustnost vln ve stejném skladu. Toto téma vysvětluje, jak nastavit metodu přidělování vln tak, aby běžela paralelně. Další informace, jak nastavit paralelní běh pro vytváření prací, najdete v tématu [Plánování vytváření práce během vlny](configure-wave-schedule-work-creation.md).

Dříve bylo možné ve skladu přidělit vždy jen jednu vlnu. Toto omezení bylo odebráno a nahrazeno novým omezením, které uzamkne pouze položku a dimenze nad umístěním v hierarchii rezervací. Dimenze nad umístěním vždy zahrnují dimenze produktu. Například pokud je položka nakonfigurována pomocí *Barva*, pak varianty pro *Červená*, *Modrá* a *Žlutá* mohou být zpracovány paralelně.

To znamená, že pokud je stejná položka se stejnými dimenzemi nad umístěním přidělena jednou vlnou, ostatní vlny budou muset počkat na získání zámku pro stejnou položku a dimenzi. Pokud zámek nelze získat včas, dojde k chybě a zpracování vlny se nezdaří.

Aby bylo možné využívat paralelní zpracování, musí vlna probíhat dávkově.

## <a name="performance-improvements"></a>Zlepšení výkonu

Výhody výkonu paralelního zpracování spadají do dvou kategorií:

- **Vylepšená propustnost** – Propustnost vln se obvykle zlepší, i když není nakonfigurováno paralelní zpracování, zejména pro scénáře, kde nedochází k překrývání položek ve vlnách.
- **Vylepšení přidělení pro jednu vlnu** – Testování zákaznických dat ukázalo téměř 50% zlepšení výkonu po přechodu na paralelní přidělení. Paralelní zpracování se provádí pro jednotlivé položky a dimenze nad umístěním, takže vylepšení závisí na tom, kolik různých položek vlna obsahuje, na dostupné infrastruktuře a době trvání přidělení oproti době trvání vytvoření práce.

## <a name="configure-parallel-allocation"></a>Konfigurace paralelního přidělení

### <a name="warehouse-management-parameters"></a>Parametry řízení skladu

Chcete-li použít zpracování paralelního přidělení, přejděte na **Řízení skladu > Nastavení > Parametry řízení skladu**, otevřete kartu **Zpracování vlny** a proveďte následující nastavení:

- **Skupina dávek pro zpracování vln** – Vyberte skupinu dávek, kterou má použít počáteční zpracování vln. Následné zpracování přidělení lze provést pomocí různých skupin dávek.
- **Zpracovat vlny v dávce** – Pro použití paralelního zpracování nastavte na *Ano*.
- **Čekat na uzamčení (ms)** – Zadejte čas v milisekundách, po který se bude v rámci kroku přidělení čekat na systémové prostředky, které jsou uzamčeny jiným krokem přidělení. Při překročení tohoto času nebude vlna zpracována a zobrazí se chybová zpráva. Doporučujeme počkat alespoň několik sekund, aby bylo možné dokončit přidělení jedné logické jednotky.

Informace o těchto a dalších možnostech zpracování vln na stránce **Parametry řízení skladu** viz [Parametry skladu pro zpracování vln](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Metody zpracování vlny

Nastavení paralelního zpracování:

1. Přejděte na **Řízení skladu > Nastavení > Vlny > Metody zpracování vlny**.
1. V mřížce vyberte metodu `allocateWave`.
1. V podokně akcí vyberte **Konfigurace úlohy**.
1. Otevře se stránka **Konfigurace úlohy metody zaúčtování vlny**. V této mřížce je uveden každý sklad, kde jste nakonfigurovali metodu `allocateWave`. Paralelní zpracování se použije pouze pro uvedené sklady. Pomocí tlačítek mna panelu akcí můžete podle potřeby přidávat nebo odebírat sklady z mřížky. 
1. U každého skladu proveďte následující nastavení:
    - **Maximální počet dávkových úloh** – Určete počet dávkových úloh, které se mají použít pro přidělení pro vybraný sklad. Optimální počet dávkových úloh závisí na dostupné infrastruktuře a na tom, jaké další dávkové úlohy se na serveru zpracovávají. Testy provedené ve čtyřjádrovém prostředí, které se zabývaly zpracování vln, ukázaly, že použití osmi úloh přineslo dobré výsledky.
    - **Skupina dávek pro zpracování vln** – Specifické skupiny dávek lze použít pro různé sklady, aby bylo možné zpracování přidělení pro škálování podle skladu.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Povolení nebo zákaz paralelizace napříč všemi právnickými osobami

Doporučujeme nastavit metodu `allocateWave`, aby běžela paralelně napříč všemi právnickými osobami, protože to pomáhá zlepšit výkon zpracování vln. Počínaje verzí Supply Chain Management 10.0.17 je funkce *Paralelizace vln pro metodu přidělení vlny* ve výchozím nastavení povolena pro všechny nové a aktualizované instalace a nelze ji znovu vypnout. Po povolení této funkce dojde k následujícímu:

- Metoda `allocateWave` je aktualizována tak, aby zahrnovala nastavení konfigurace úlohy, které vám umožní používat stránku **Metody zpracování vlny** k definování počtu úloh, které budou spuštěny současně, ekvivalentní počtu paralelních procesů. Výsledkem je, že čas strávený krokem přidělení vlny (což je obvykle 30–60 % celkového času zpracování) je snížen o faktor, který je zhruba ekvivalentní počtu úloh. Je také možné vybrat, která dávka bude přiřazena ke zpracování těchto úloh. Je důležité si uvědomit, že všechny vaše právnické osoby budou nakonfigurovány pro dávkové zpracování vln. Pro sklady, které jsou již nakonfigurovány pro dávkové zpracování vln, a pro sklady, které jsou již nakonfigurovány pro paralelní použití metody `allocateWave`, zůstane zachována stávající konfigurace.
- Ve výchozím nastavení jsou všechny nové právnické osoby nakonfigurovány pro dávkové zpracování vln. Všechny nové sklady s povolenou možností **Procesy řízení skladu** budou mít ve výchozím nastavení nakonfigurovanou metodu `allocateWave` pro paralelní běh.
- Na stránce **Parametry řízení skladu** je možnost **Zpracovat vlny v dávce** nastavena na *Ano* a **Čekat na uzamčení (ms)** na výchozích 15 sekund. To znamená, že všechny vlny budou provedeny v dávce. Když je vlna spuštěna, získá během kroku přidělení zámek na položku a dimenze nad umístěním. Když se další úloha zpracování vlny pokusí získat stejný zámek pro identický záznam, zablokuje se až do dokončení aktuálního zpracování. Nastavení **Čekat na uzamčení (ms)** určuje maximální dobu, po kterou bude systém čekat, než se zámek uvolní.

Paralelní zpracování přidělení vyžaduje dávkové zpracování vlny. Proto snížíte výkon zpracování vlny, pokud vypnete nastavení **Zpracovat vlny v dávce**, zejména pokud zpracování vln používá paralelní proces definovaný v konfiguraci úlohy pro příslušné metody vln.

Je-li to nutné, můžete vrátit všechna nastavení provedená ve výchozím nastavení, kdy je pro vaši instanci automaticky povolena funkce *Paralelizace vln pro metodu přidělení vlny*. Postup je následující:

- Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**. Na kartě **Zpracování vln** použijte preferované hodnoty pro možnosti **Zpracovat vlnu v dávce** a **Čekat na zámek (ms)**.
- Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**. Vyberte metodu `allocateWave`. V podokně akcí vyberte **Konfigurace úlohy** pro otevření stránky, která obsahuje každý sklad, kde je nastavena paralelní metoda. Podle potřeby upravte nebo odstraňte počet dávkových úkolů a přiřazenou skupinu vln pro každý uvedený sklad.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="troubleshoot-using-the-infolog"></a>Odstraňování problémů pomocí informačního protokolu

Protože se používá rozhraní dávek, chyby, které se vyskytnou během zpracování vln, budou zachyceny jako součást informačního protokolu dávkových úloh. Jak číst dávkové úlohy související s vlnou:

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte vlnu, které chcete zkontrolovat.
1. V podokně akcí otevřete kartu **Vlna** a ve skupině **Vlna** zvolte **Dávkové úlohy**.

Zpracování vln je samoopravné, takže všechny chyby zjištěné během zpracování by měly být vykázány v informačním protokolu.

Typickou chybou související s paralelním zpracováním může být to, že dvě vlny se pokusí přidělit stejnou položku ve stejnou dobu a jedna se nedokončí, takže druhá vlna není schopna získat zámek ve stanoveném čase. Pokud tato situace nastane, protokol dávkových úloh bude obsahovat informace, že zámek pro položku nelze získat, a v takovém případě musí být vlna, která selhala, znovu zpracována.

Protože zpracování probíhá paralelně, je nutné data sledovat v různých tabulkách, aby bylo možné sledovat stav zpracování. To znamená, že protokoly pro dávkové úlohy mohou obsahovat chyby, například chyby duplicitních klíčů.

Chyby dávkových úloh jsou také součástí protokolu dávkových úloh. Nejdůležitější informace jsou obvykle ve spodní části.

Ve vzácných případech, například pokud bylo ukončeno připojení SQL, je možné, že zpracování vlny skončí v nekonzistentním stavu, kdy se zdá, že je spuštěna dávková úloha, ale zpracování je zastaveno. Vlna nedokáže takové chyby zpracovat, takže pokus o vyčištění neúspěšných vln je proveden při běhu následující vlny. Alternativně, pokud je aktuální vlna v nekonzistentním stavu, proveďte následující kroky:

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte vlnu, kterou potřebujete vyčistit.
1. V podokně akcí otevřete kartu **Vlna** a ve skupině **Vlna** zvolte **Vyčistit data vlny**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Odstraňování problémů pomocí protokolu průběhu vlny

Pokud je povolena možnost **Vytvořit protokol průběhu vlny** na stránce **Parametry řízení skladu**, pak se při každém zahájení a ukončení přidělení položky a jejích dimenzí vytvoří záznam protokolu. Tento protokol byste měli povolit, pouze když ho potřebujete, například při počátečním testování nebo při řešení potíží. Pokud je tato možnost povolena, můžete protokol zobrazit následujícím způsobem:

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte vlnu, které chcete zkontrolovat.
1. V podokně akcí otevřete kartu **Vlna** a ve skupině **Vlna** zvolte **Průběh**.
