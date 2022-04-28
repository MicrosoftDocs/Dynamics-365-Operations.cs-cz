---
title: Naplánujte čištění dat historie prodeje
description: Toto téma popisuje, jak můžete zlepšit výkon systému naplánováním pravidelné úlohy čištění historie aktualizací prodeje v pravidelných intervalech.
author: myvakalo
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6c6c1e08d45f2a7d1e1267010b286111bad01a6c
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570355"
---
# <a name="schedule-sales-history-data-cleanup"></a>Naplánujte čištění dat historie prodeje

[!include [banner](../includes/banner.md)]

V rámci svého standardního provozu Microsoft Dynamics 365 Supply Chain Management generuje a ukládá průběžně aktualizovaná data historie prodeje. Postupem času se ve vašem systému může nashromáždit velké množství zastaralých dat historie prodeje. Tato nashromážděná data mohou způsobit problémy s výkonem a funkčností při zaúčtování dokladů souvisejících s prodejními objednávkami. (Tyto dokumenty zahrnují potvrzení prodejní objednávky, prodejní balicí listy, seznamy odběrů a faktury). Proto byste měli nastavit a naplánovat pravidelnou úlohu *Vyčištění historie aktualizace prodeje* spouštěnou v pravidelných intervalech. Tato úloha odstraní všechna data aktualizace historie prodeje, která již nejsou potřeba.

Pokud použijete pravidelnou úlohu *Vyčištění historie aktualizace prodeje*, doporučujeme povolit funkci *Zlepšení výkonu čištění historie prodeje*, díky které bude úloha probíhat efektivněji. (Nicméně úlohu můžete spustit i bez povolení této funkce.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Zapněte funkce čištění historie prodeje

Chcete-li nastavit a používat pravidelnou úlohu *Vyčištění historie aktualizace prodeje* spolu se všemi funkcemi, které jsou popsány v tomto tématu, musíte povolit funkce *Zlepšení výkonu čištění historie prodeje* a *Vyčistěte historii aktualizací prodeje na základě stáří* ve správě funkcí, jak je popsáno v následujících podsekcích.

### <a name="sales-history-cleanup-performance-improvements"></a>Vylepšení výkonu čištění historie prodeje

Pravidelná dávková úloha **Vyčištění historie prodeje** může trvat dlouho, pokud se zřídka spouští v prostředích s velkým objemem aktualizací prodeje. V těchto situacích funkce *Vylepšení výkonu vyčištění historie prodeje* může pomoci zkrátit dobu běhu a zlepšit spolehlivost.

Tato funkce zlepšuje stávající úlohu vyčištění následujícími způsoby:

- Rozděluje vyčištění na dávky (velikost dávky můžete změnit pomocí přizpůsobení).
- Poběží maximálně 2 hodiny (dobu trvání můžete změnit pomocí přizpůsobení).
- Kde je to možné, využívá se možnosti databáze, aby se minimalizovalo omezení zamykáním a zabránilo se spojování transakčních tabulek během čištění.

Po aktivaci funkce dávková úloha **Vyčištění historie aktualizace prodeje** (**Prodej a marketing \> Pravidelné úkoly \> Čištění \> Vyčištění historie aktualizace prodeje**) poběží jako předtím, ale s lepším výkonem a maximálně 2 hodiny. To znamená, že může být nutné několikrát spustit, abyste vyčistili všechna data pro konkrétní časový rámec uchování.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Přehled prodeje a marketingu*
- **Název funkce:** *Vylepšení výkonu čištění historie prodeje*

### <a name="clean-up-sales-update-history-based-on-age"></a>Vyčistění historie aktualizace prodejů na základě stáří

Funkce *Vyčistění historie aktualizace prodejů na základě stáří* umožňuje nastavit maximální stáří záznamů, které se mají uchovávat při spuštění periodické úlohy *Vyčištění historie aktualizace prodeje*. Starší záznamy budou smazány. Tato funkce je užitečná, když nastavíte pravidelné spouštění úlohy, protože stáří se vždy počítá vzhledem k datu spuštění úlohy. Pokuf tuto funkci nepoužijete, můžete nastavit pouze konkrétní datum pro uchování nejstarších záznamů.

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Přehled prodeje a marketingu*
- **Název funkce:** *Vyčistění historie aktualizace prodejů na základě stáří*

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Nastavte a naplánujte pravidelnou úlohu čištění historie prodeje

Chcete-li nastavit naplánovat pravidelnou úlohu *Čištění historie prodeje*, postupujte následovně.

1. Analyzujte své obchodní potřeby a určete, kolik dní historických dat zaúčtování prodejní objednávky musíte uchovávat. Obvykle doporučujeme spouštět úlohu čištění každé tři měsíce a maximálně každých šest měsíců.
1. Přejděte na **Prodej a marketing \> Pravidelné úlohy \> Čištění \> Vyčištění historie aktualizace prodeje**.
1. V dialogovém okně **Vyčistit historii aktualizací prodeje** na pevné záložce **Parametry** nastavte následující pole:

    - **Vyčistit** – Vyberte jednu z následujících hodnot pro určení typu záznamů, které se mají vyčistit:

        - **Provedené** – Odstraňte pouze záznamy, které byly plně zpracovány. Protože je nepravděpodobné, že byste tyto záznamy mohli dále používat, je tato možnost nejbezpečnější.
        - **Provedené a chybné** – Odstraňte jak plně zpracované záznamy, tak záznamy, kde došlo k chybě. Tato možnost je nejčastěji používaná. Možná budete chtít zkontrolovat a dokonce opravit chybné záznamy místo toho, abyste je nechali automaticky čistit. Mnoho společností se však asi po měsíci rozhodlo vyčistit i tyto záznamy, protože v té době již pravděpodobně nejsou relevantní.
        - **Všechno** – Odstraňte provedené, chybné a čekající záznamy. Záznamy o čekání jsou platné, ale ještě nebyly plně zpracovány. Ve většině případů pravděpodobně nechcete, aby byly automaticky smazány. V některých situacích však můžete zvolit jejich automatické smazání po uplynutí určité doby.

    - **Uchovávejte záznamy podle stáří** – Určete, zda chcete vyčistit záznamy na základě jejich stáří v den, kdy byla úloha spuštěna, nebo odstranit záznamy, které byly vytvořeny před pevným datem. Pokud plánujete čištění jako opakovanou úlohu, měli byste tuto možnost nastavit na *Ano*, protože stáří se vždy počítá vzhledem k datu spuštění úlohy.

        - Nastavte turo možnost na *Ano* a povolte tak pole **Maximální stáří**. Toto pole se používá k určení maximálního stáří záznamů, které se mají zachovat při každém spuštění úlohy. Pole **Vytvořeno do** je ignorováno.
        - Nastavte turo možnost na *Ne* a povolte tak pole **Vytvořeno do**. Toto pole se používá k určení nestaršího data vytvoření, které se mají zachovat při spuštění úlohy. Pole **Maximální stáří** je ignorováno.

    - **Vytvořeno do** – Toto nastavení platí pouze tehdy, když je možnost **Uchovávejte záznamy podle stáří** nastavena na *Ne*. Zadejte nestarší datum vytvoření, které se mají zachovat při spuštění úlohy. Záznamy vytvořené před tímto datem budou smazány.
    - **Maximální stáří** – Toto nastavení platí pouze tehdy, když je možnost **Uchovávejte záznamy podle stáří** nastavena na *Ano*. Zadejte maximální stáří (ve dnech) záznamů, které se mají zachovat při každém spuštění úlohy. Starší záznamy budou smazány.

1. N záložce s náhledem **Spustit na pozadí** určete, kdy a jak často bude úloha spuštěna. Tato nastavení použijte k implementaci plánu, který jste určili v kroku 1. Pole fungují stejně jako u jiných typů [dávkových úloh](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno.
