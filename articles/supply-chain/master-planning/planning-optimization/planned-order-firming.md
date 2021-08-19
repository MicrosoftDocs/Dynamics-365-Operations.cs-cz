---
title: Potvrdit plánované objednávky
description: Toto téma vysvětluje, jak potvrdit plánované objednávky. Při potvrzení jsou plánované objednávky transformovány do skutečných nákupních objednávek, převodních příkazů nebo výrobních zakázek.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 966a878a7e5b0a92d6d53e67bea19c50274087a4416980859175b12c6fdfbcdc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764829"
---
# <a name="firm-planned-orders"></a>Potvrdit plánované objednávky

[!include [banner](../../includes/banner.md)]

Plánované objednávky musí být *potvrzeny* (tj. uvolněny) jako součást procesu hlavního plánování. Při potvrzení jsou plánované objednávky transformovány do skutečných nákupních objednávek, převodních příkazů nebo výrobních zakázek. Tyto objednávky jsou známy také jako *vydané* objednávky nebo *otevřené* objednávky.

Existují tři způsoby, jak plánované objednávky potvrdit:

- **Ruční potvrzení** - Vyberte konkrétní plánované objednávky v seznamu a poté proces spusťte ručně.
- **Automatické potvrzení** - Definujte výchozí časové zpoždění pro skupiny pokrytí, jednotlivé položky a kombinace položek a hlavních plánů. Poté se během běhů hlavního plánování plánované objednávky automaticky zpracují, pokud je datum objednávky ve stanovené ochranné době pro potvrzení.
- **Potvrzení založené na dotazech** - Definujte dotaz pro výběr plánovaných objednávek na základě jejich vlastností. Můžete nastavit dávkovou úlohu pro pravidelné spouštění dotazů a pevných párovacích objednávek.

Toto téma podrobně popisuje každou metodu.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Povolte funkce popsané v tomto tématu

Většina funkcí plánované objednávky je k dispozici ve všech standardních instalacích Microsoft Dynamics 365 Supply Chain Management které používají optimalizace plánování. Než však budete moci používat funkce, které jsou popsány v tomto tématu, musí být ve Správci funkcí zapnuté.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Zapněte paralelizované potvrzení plánovaných objednávek

Paralelizované potvrzování pomáhá urychlit proces zpevnění tím, že jej paralelizuje napříč více vlákny. Tento přístup může být užitečný, když je spuštěno mnoho plánovaných objednávek.

Chcete-li tuto funkci ve svém systému zpřístupnit, přejděte na [Správu funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Paralelní potvrzení plánovaných objednávek*.

### <a name="enable-planned-order-firming-with-filtering"></a>Povolte plánované potvrzení objednávky pomocí filtrování

Zpracování plánovaných objednávek s filtrováním vám umožňuje definovat logická kritéria pro výběr plánovaných objednávek, které se mají potvrdit. Můžete také zobrazit náhled vybraných plánovaných objednávek, spustit proces na pozadí nebo jej naplánovat jako dávkovou úlohu.

Chcete-li tuto funkci ve svém systému zpřístupnit, přejděte na [Správu funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Zpracování plánovaných objednávek s filtrováním*.

### <a name="enable-auto-firming-for-planning-optimization"></a>Zapněte automatické potvrzení pro optimalizací plánování

Automatické potvrzení umožňuje potvrdit plánované objednávky v rámci procesu hlavního plánování během ochranné doby pro potvrzení. Automatické plánování je vždy podporováno pro plánovací modul zabudovaný do Supply Chain Management. Chcete-li ji však použít také s optimalizací plánování, musíte tuto funkci zapnout.

Chcete-li tuto funkci ve svém systému zpřístupnit, přejděte na [Správu funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Automatické potvrzení pro optimalizaci plánování*.

## <a name="manually-firm-planned-orders"></a>Manuálně potvrďte plánované objednávky

Chcete-li ručně zpracovat plánované objednávky, vyhledejte a vyberte plánované objednávky, které chcete potvrdit, a poté ručně spusťte proces potvrzení.

1. [Otevřete stránku se seznamem plánovaných objednávek](approved-planned-order.md#view-planned-orders).
1. Použijte pole **Filtr**, **Plán** a záhlaví sloupců pro filtrování a řazení seznamu, abyste mohli najít plánované objednávky, které hledáte.
1. Zaškrtněte políčko pro každou naplánovanou objednávku, kterou chcete potvrdit. Pokud chcete potvrdit všechny plánované objednávky, které jsou aktuálně uvedeny na stránce (na základě filtrů, které jste použili), tento krok přeskočte.
1. V podokně akcí vyberte jedno z následujících tlačítek:

    - **Potvrdit** - Potvrďte pouze vybrané plánované objednávky.
    - **Potvrdit vše** - Potvrďte všechny plánované objednávky, které jsou aktuálně uvedeny na stránce (na základě filtrů, které jste použili), bez ohledu na zaškrtnutá políčka. Tato možnost může být užitečná v případě, že potvrzujete vysoký počet plánovaných objednávek.

1. V dialogovém okně **Potvrzení** na záložce **Parametry** nastavte následující pole. (Mnoho z těchto polí přebírá své výchozí hodnoty ze záložky **Standardní aktualizace** na stránce **Parametry hlavního plánování**.)

    - **Aktualizovat označení** - Vyberte pravidla značení zásob, která se použijí při potvrzování plánovaných objednávek.
    - **Zastavit potvrzování, dojde-li k chybě** - Nastavte tuto možnost na *Ano* pro zastavení potvrzování všech vybraných plánovaných objednávek, pokud dojde k chybě v jedné z nich. Tato možnost musí být nastavena na *Ne* pokud je možnost **Paralelizovat potvrzení** nastavena na *Ano*.
    - **Paralelizovat potvrzení** - Tato možnost je k dispozici pouze pokud je funkce [*Paralelní potvrzení plánovaných objednávek*](#enable-features) ve vašem systému zapnutá a pokud jste vybrali dvě nebo více plánovaných objednávek ke spuštění. Nastavte ji na *Ano* pro paralelní běh potvrzovacích procesů. Paralelní potvrzování může zlepšit výkon.
    - **Počet vláken** - Tato možnost je k dispozici pouze pokud je funkce [*Paralelní potvrzení plánovaných objednávek*](#enable-features) ve vašem systému zapnutá a pokud jste nastavili možnost **Paralelizovat potvrzení** na *Ano*. Zadejte počet vláken, které se mají použít k paralelizaci procesu potvrzování. Informace o tom, jak použít tuto možnost v hlavním plánování, najdete v části [Vylepšení výkonu hlavního plánování](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Hodnota *0* (nula) pro pole **Počet vláken** zvyšuje operační čas hlavního plánování. Proto doporučujeme, abyste vždy nastavili hodnotu tohoto pole na hodnotu větší než 0.

    - **Seskupit podle dodavatele** - Nastavte tuto možnost na *Ano* pro seskupení plánovaných nákupních objednávek a vytvoření jedné nákupní objednávky na dodavatele během spouštění. Případně lze vytvořit jednu nákupní objednávku s jedním řádkem pro každou plánovanou objednávku.
    - **Seskupit podle skupiny nákupčích** - Tuto možnost nastavte na *Ano*, pokud má skupina plánovaných objednávek tvořit jedinou nákupní objednávku, která slučuje skupinu dodavatele a nákupčího. Pro použití této možnosti je také nutné nastavit možnost **Seskupit podle dodavatele** na *Ano*.
    - **Seskupit podle kupní smlouvy** - Nastavte tuto možnost na *Ano*, chcete-li seskupit plánované nákupní objednávky, které mají stejného dodavatele jako stávající nákupní smlouvy, a vytvořit jednu nákupní objednávku na každou smlouvu. Tato možnost je automaticky povolena, když je povolena možnost **Seskupit podle dodavatele**. Chcete-li použít **Seskupit podle kupní smlouvy**, možnost **Najděte kupní smlouvu** musí být nastavena na *Ano* na stránce **Hlavní plánovací parametry**.
    - **Seskupit podle období** (v části **Nákupní objednávky**) - Vyberte období, do kterého chcete seskupit plánované nákupní objednávky. Pro použití této možnosti je také nutné vybrat možnost **Seskupit podle dodavatele**.
    - **Seskupit podle období** (v části **Převody**) - Vyberte období, do kterého chcete seskupit plánované převodní příkazy. Objednávky budou seskupeny podle hodnot **Ze skladu** a **Do skladu**.

    ![Záložka s náhledem Parametry v dialogovém okně Potvrzení.](./media/manual-firming.png "Záložka s náhledem Parametry v dialogovém okně Potvrzení")

1. Na záložce s náhledem **Spustit na pozadí**, nastavte úlohu tak, aby běžela v dávkovém režimu. Nemá však smysl nastavovat opakovaný plán, když provádíte ruční potvrzování. Pole fungují stejně jako u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management. U ručního zpracování však bude dávková úloha zpracovávat pouze aktuálně vybrané plánované objednávky. Nebude zpracovávat žádné objednávky, které odpovídají filtrům, které jsou aktuálně použity na stránce.
1. Vyberte **OK**, pokud chcete použít své nastavení a vygenerovat potvrzené objednávky.

## <a name="auto-firm-planned-orders"></a>Automaticky potvrdit plánované objednávky

Automatické potvrzení umožňuje potvrdit plánované objednávky v rámci procesu hlavního plánování. Můžete definovat výchozí časové zpoždění pro skupiny pokrytí, jednotlivé položky a kombinace položek a hlavních plánů. Poté se během běhů hlavního plánování plánované objednávky automaticky zpracují, pokud je datum objednávky ve stanovené ochranné době pro potvrzení. Plánované objednávky, které jsou generovány Optimalizací plánování a integrovanou operací plánování, zpracovávají datum objednávky (tj. počáteční datum) odlišně.

> [!NOTE]
> K automatickému potvrzení plánovaných nákupních objednáevk může dojít pouze tehdy, pokud je položka přidružena k dodavateli.
> 
> Odvozené objednávky (nákupní objednávky dílčí smlouvy) které jsou potvrzeny budou zobrazovat stav *Probíhá kontrola*, když je povoleno sledování změn případů.

> [!IMPORTANT]
> Předtím, než lze funkci popsanou v této části použít s Optimalizací plánování, vlastnost [*Automatické potvrzení pro optimalizaci plánování*](#enable-features) musí být ve vašem systému zapnuta, jak je popsáno na začátku tohoto tématu. Automatické potvrzování lze vždy použít s vestavěným hlavním plánovacím modulem.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatické potvrzování s Optimalizací plánování vs. vestavěný plánovací modul

Optimalizaci plánování i integrovaný plánovací modul lze použít k automatickému potvrzování plánovaných objednávek. Existují však některé důležité rozdíly. Pokud například optimalizace plánování použije datum objednávky (tj. počáteční datum) k určení, které plánované objednávky mají být potvrzeny, použije předdefinovaný modul plánování datum požadavku (tj. koncové datum). Rozdíly jsou shrnuty v následující tabulce.

| Funkce | Optimalizace plánování | Integrovaný plánovací modul |
|---|---|---|
| **Základ data** | Automatické potvrzení je založeno na datu objednávky (počáteční datum). | Automatické potvrzení je založeno na datu požadavku (koncové datum). |
| **Doba realizace** | Vzhledem k tomu, že datum objednávky (počáteční datum) aktivuje potvrzení, nemusíte považovat dobu realizace za součást ochranné doby potvrzení. | Chcete-li zajistit, aby byly příkazy potvrzeny včas, musí být ochranná doba potvrzení delší než doba realizace. |
| **Objednávky pro aktuální týden** | Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování jeden týden. | Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování doba realizace plus jeden týden. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Nastavení automatického potvrzení a ochranná doba potvrzení

Automatické potvrzení zapnete přiřazením časového ohraničení automatického zpevnění příslušnému nastavení pokrytí, jak je popsáno dále v této části. Pokud automatické nastavení není zapnuto pro jakékoli nastavení pokrytí, nebo pokud je plánování spuštěno z konkrétní stránky, například ze stránky **Čisté požadavky** pro uvolněný produkt, je proces automatického potvrzení přeskočen.

Možnosti seskupení a označení pro automatické potvrzení berou jejich hodnoty ze záložky **Standardní aktualizace** na stránce **Hlavní plánovací parametry**.

Ochranná doba automatického potvrzení je definována počtem dní, které zadáte pro příslušné nastavení pokrytí. Ochrannou dobu automatického potvrzování můžete spustit a řídit následujícími způsoby:

- Chcete-li definovat výchozí ochrannou dobu potvrzování pro skupinu disponibility, přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Skupiny disponibility** a vyberte skupinu disponibility. Pak na pevné záložce **Jiné** zadejte do pole **Ochranná doba automatického potvrzování (ve dnech)** počet dní.
- Chcete-li přepsat ochrannou dobu potvrzování, která je definována pro skupinu disponibility pro konkrétní položku, přejděte na **Správa informací o produktu \> Vydané produkty**. V podokně akcí vyberte **Plánování** a pak vyberte **Disponibilita položky**. Na kartě **Obecné** vyberte **Přepsat ochrannou lhůtu** a do pole **Automatická ochranná lhůta (dny)** zadejte počet dní.
- Chcete-li přepsat ochrannou dobu potvrzování definovanou pro skupinu disponibility a disponibilitu položky pro určitý hlavní plán, přejděte na **Hlavní plánování \> Nastavení \> Hlavní plány** a vyberte hlavní plán. Pak na pevné záložce **Ochranná doba ve dnech** nastavte možnost **Potvrzení** na *Ano* a zadejte počet dní.

Pokud nastavíte všechny výše uvedené ochranné doby na *0* (nula), automatické vypínání je u příslušných krytých položek účinně deaktivováno.

## <a name="firm-planned-orders-by-using-a-query"></a>Zpracování plánovaných objednávek pomocí dotazu

Zpracování založené na dotazech umožňuje plánovat potvrzení na základě předem definovaných kritérií. Na rozdíl od automatického potvrzování umožňuje zpoždění založené na dotazech automatické zpevnění různých podskupin objednávek v různých časových bodech. Dále můžete použít manuální nebo automatizované operace k potvrzení různých typů plánovaných objednávek. Můžete si také prohlédnout, které potvrzené objednávky jsou vybrány na základě vašeho nastavení. Proto můžete potvrdit, že výběr odpovídá vašim očekáváním.

Můžete kombinovat automatické potvrzování se zpožděním založeným na dotazech. Například úloha potvrzení na základě dotazu má ochranné období, které je delší než ochranné období pro odpovídající konfiguraci pokrytí automatickým zpevněním. Potvrzení úlohy založené na dotazu proto zpracuje plánované objednávky před spuštěním automatického potvrzení. Toto chování můžete využít k naplánování objednávek pro konkrétní dodavatele odlišně od objednávek podobných produktů od jiných dodavatelů.

> [!IMPORTANT]
> Předtím, než lze funkci popsanou v této části použít, vlastnost [*Zpracování plánovaných objednávek s filtrováním*](#enable-features) musí být ve vašem systému zapnuta, jak je popsáno na začátku tohoto tématu.

Chcete-li naplánovanou objednávku potvrdit pomocí procesu potvrzení na základě dotazu, postupujte takto.

1. Přejděte na **Hlavní plánování \> Hlavní plánování \> Spustit \> Zpracování plánovaných objednávek**.
1. V dialogovém okně **Plánované potvrzení objednávky** na záložce s náhledem **Parametry** nastavte základní možnosti zpracování, značení a seskupování. Tyto možnosti fungují stejně jako v dialogovém okně **Potvrzování**. (Pro popis viz předchozí část.) Poté v části **Plán** nastavte následující pole, která jsou jedinečná pro dialogové okno **Zpracování plánovaných objednávek**:

    - **Plán** - Vyberte hlavní plán, který by se měl použít při potvrzování plánovaných objednávek nalezených tímto dotazem.
    - **Počet dní dopředu pro ochrannou dobu potvrzení** - Vyberte, jak daleko v budoucnosti musí být různé požadavky a další ohledy vypočítány podle hlavního plánování.
    - **Počet dní dozadu pro ochrannou dobu potvrzení** - Vyberte, jak daleko v minulosti musí být různé požadavky a další ohledy vypočítány podle hlavního plánování.

    ![Záložka s náhledem Parametry v dialogovém okně Zpracování plánovaných objednávek.](./media/planned-order-firming-main-1.png "Záložka s náhledem Parametry v dialogovém okně Zpracování plánovaných objednávek")

1. Chcete-li určit, které záznamy by měly být zahrnuty do objednávky, vyberte tlačítko **Filtr** na záložce s náhledem **Záznamy, které mají být zahrnuty**. Zobrazí se standardní dialogové okno dotazu, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Supply Chain Management. Pole zde jsou jen pro čtení a zobrazují hodnoty, které se vztahují k vašemu dotazu.

    ![Záložka s náhledem Zahrnuté záznamy v dialogovém okně Zpracování plánovaných objednávek.](./media/planned-order-firming-main-2.png "Záložka s náhledem Zahrnuté záznamy v dialogovém okně Zpracování plánovaných objednávek")

1. Vyberte **Náhled** k náhledu obsahu potvrzené objednávky na základě vašeho dosavadního nastavení. Seznam plánovaných objednávek, které budou zpracovány, se zobrazí jako zpráva. Poté můžete podle potřeby upravit svá nastavení, dokud náhled neukáže potvrzenou objednávku tak, jak ji zamýšlíte.

    ![Příklad náhledu potvrzené objednávky.](./media/planned-order-firming-preview.png "Příklad náhledu potvrzené objednávky")

    > [!WARNING]
    > Tato funkce potvrdí všechny plánované objednávky, které odpovídají kritériím filtru. Nekritické potvrzování plánovaných objednávek může způsobit vytvoření obrovského počtu nechtěných nákupních, převodových a výrobních objednávek. Než budete pokračovat, vždy použijte tlačítko **Náhled** k ověření záznamů, které budou zahrnuty.

1. Na záložce s náhledem **Spustit na pozadí**, nastavte úlohu tak, aby běžela v dávkovém režimu a/nebo nastavit opakující-se rozvrh. Pole fungují stejně jako u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Vyberte **OK**, pokud chcete použít své nastavení a vygenerovat potvrzené objednávky.

## <a name="track-firmed-orders"></a>Sledujte potvrzené objednávky

Chcete-li sledovat plánovanou objednávku, která byla poslána, postupujte takto.

1. [Otevřete stránku se seznamem plánovaných objednávek](approved-planned-order.md#view-planned-orders).
1. Vyberte nebo otevřete plánovanou objednávku, kterou chcete sledovat.
1. V podokně akcí na kartě **Zobrazit** ve skupině **zobrazení** vyberte **Historie potvrzování**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
