---
title: Opětovné přidělení uznání výnosů
description: Tento článek popisuje opětovné přidělení, které organizacím umožňuje přepočítat výnosové ceny při změně podmínek smluvního prodeje. Téma obsahuje odkazy na další témata, která popisují, jak uznat výnosy v různých situacích.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a79288fd69a2e7780ff03952b05b99db2ed88e41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903413"
---
# <a name="revenue-recognition-reallocation"></a>Opětovné přidělení uznání výnosů

[!include [banner](../includes/banner.md)]

Opětovné přidělení umožňuje organizacím přepočítat výnosové ceny při změně podmínek smluvního prodeje. Při uznání výnosů jsou dokumenty prodejní objednávky považovány za smlouvu.

Vaše organizace se musí rozhodnout, zda je opětovné přidělení nutné. Přidání nového řádku na prodejní objednávku nebo vytvoření nové prodejní objednávky pro odběratele nemusí znamenat změnu smlouvy. Opětovné přidělení může být potřeba v následujících situacích.

- Odběratel přidal položky na prodejní objednávku nebo odstranil položky z prodejní objednávky poté, co byla objednávka plně nebo částečně fakturována.
- Pro jednu sjednanou smlouvu bylo zadáno více prodejních objednávek, ať už v potvrzeném, nebo fakturovaném stavu.
- Odběratel vrátil nebo obdržel kredit za položku poté, co byla původní prodejní objednávka zcela nebo částečně fakturována.

Proces opětovného přidělení má několik důležitých omezení:

- Lze jej spustit pouze jednou. Proto je důležité, abyste jej spustili až po dokončení všech změn.

    - Toto omezení je odstraněno ve vydané verzi 10.0.17 a novější.

- Proces nelze spustit pro prodejní objednávky projektu.

    - Toto omezení je odstraněno ve vydané verzi 10.0.17 a novější.

- Pokud se jedná o více prodejních objednávek, musí být pro stejný účet odběratele.
- Všechny opětovně přidělené prodejní objednávky musí mít stejnou měnu transakce.
- Proces nelze po jeho spuštění stornovat, ani vrátit zpět.

    - Toto omezení je odstraněno ve vydané verzi 10.0.17 a novější.

- Opětovné přidělení lze provést pouze u prodejních objednávek nebo projektových prodejních objednávek. Nelze jej provést u kombinace prodejních objednávek a projektových prodejních objednávek.

    - Toto omezení je odstraněno ve vydané verzi 10.0.17 a novější.

## <a name="set-up-reallocation"></a>Nastavení opětovného přidělení

Proces opětovného přidělení ovlivňuje jeden parametr.

Protože opětovné přidělení lze provést pro částečně nebo plně fakturovanou prodejní objednávku, všechny předchozí účetní položky faktury musí být opraveny pomocí nových, opětovně přidělených výnosových cen. Tato oprava spočívá ve stornování účetní položky původní faktury a zaúčtováním nové účetní položky na základě opětovně přidělených výnosových cen.

Každá organizace se musí rozhodnout, zda má oprava aktualizovat pouze hlavní knihu, nebo také pohledávky. Přijaté rozhodnutí určí vhodné nastavení možnosti **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na kartě **Uznání výnosů** na stránce **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**). Příslušná nastavení závisí na konkrétní situaci. Další informace o možných situacích získáte pod odkazy v sekci [Scénáře, kdy lze použít opětovné přidělení](#scenarios-for-reallocation) dále v tomto článku.

[![Karta Uznání výnosů na stránce Parametry hlavní knihy](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Pokud je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** nastavena na **Ano**, proces opětovného přidělení skončí tímto výsledkem:

- Kvůli stornování faktury, která vyžaduje opravu, je v pohledávkách vytvořen dokument akreditivu.

    - Dokument akreditivu znovu použije číslo původní faktury, ke kterému je připojen řetězec „-1“.
    - Dokument akreditivu se automaticky vyrovná podle původní faktury. Pokud již byla původní faktura vyrovnána jiným dokumentem akreditivu nebo platbou, toto vyrovnání je automaticky stornováno.
    - Dokument akreditivu se zaúčtuje do hlavní knihy kvůli a stornuje účetní položku, která byla zaúčtována na původní faktuře. Položky transakcí zásob a nákladů prodaného zboží (COGS) však stornovány nejsou.

- V pohledávkách je vytvořena nová faktura, která vychází z nových, opětovně přidělených částkách ceny.

    - Nová faktura znovu použije číslo původní faktury, ke kterému je připojen řetězec „-2“.
    - Nová faktura se automaticky vyrovná podle všech dokumentů akreditivů nebo plateb, které byly dříve vyrovnány podle původní faktury.
    - Nová faktura se zaúčtuje do hlavní knihy pomocí nových, opětovně přidělených částek výnosových cen. Faktura není opětovně zaúčtována do účtů zásob a COGS, protože tyto položky jsou zachovány v účetní položce na původní faktuře.

Pokud je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** nastavena na **Ne**, proces opětovného přidělení skončí tímto výsledkem:

- Stornovací účetní položka se zaúčtuje pouze do hlavní knihy. Veškeré účetnictví původní faktury je stornováno, kromě účetních položek zásob a COGS.
- Nová účetní položka se zaúčtuje pouze do hlavní knihy na základě nových, opětovně přidělených výnosových cen. Faktura není opětovně zaúčtována do účtů zásob a COGS, protože tyto položky jsou zachovány v účetní položce na původní faktuře.
- Faktura na stránce **Transakce odběratele** není nijak ovlivněna ani změněna, ale stále uvádí původní účetní položku. Pro stornovací nebo nové účetní položky neexistuje žádný odkaz.

Jak již bylo zmíněno, můžete aktualizovat pouze hlavní knihu, nebo můžete aktualizovat jak hlavní knihu, tak pohledávky. Oba přístupy mají klady a zápory. Doporučujeme vyhodnotit požadavky vaší organizace a podle toho se rozhodnout pro jednu z možností. Pokud aktualizujete hlavní knihu i pohledávky, nová faktura bude obsahovat správné účetní položky, které lze zobrazit z dokumentu na stránce **Transakce odběratele**. Mimo to použije proces vyrovnání aktualizované účetní položky k zaúčtování peněžních slev a zisků nebo ztrát. Na druhou stranu se dokument akreditivu a nová faktura objeví ve výpisech z účtu odběratele a v sestavách prodlení, jako tomu je u ostatních dokumentů akreditivu a faktur odběratelů. Popis těchto dokumentů bude obsahovat informaci, že byly vytvořeny při opravě účetnictví.

## <a name="run-the-reallocation-process"></a>Spuštění procesu opětovného přidělení

Proces opětovného přidělení spustíte tlačítkem **Opětovné přidělení ceny k novým řádkům objednávky** v prodejní objednávce, kterou musíte znovu přidělit. Případně přejděte na **Uznání výnosů \> Pravidelné úkoly \> Opětovné přidělení ceny k novým řádkům objednávky** a poté zadejte příslušné filtry, například účet odběratele.

[![Opětovné přidělení ceny k novým řádkům objednávky](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Horní mřížka na stránce **Opětovné přidělení ceny k novým řádkům objednávky** je pojmenována **Prodej**. Tato mřížka obsahuje seznam prodejních objednávek odběratele. Vyberte prodejní objednávky, které je třeba opětovně přidělit. Pokud má prodejní objednávka ID opětovného přidělení, už byla označena pro opětovné přidělení jiným uživatelem. Pokud byly jedna nebo více prodejních objednávek dříve opětovně přiděleny a musí být zahrnuty do jiného opětovného přidělení, musí být opětovné přidělení těchto prodejních objednávek nejprve zrušeno. Poté mohou být zahrnuty do nového opětovného přidělení. Podrobnější informace najdete v částech [Vrátit zpět opětovné přidělení](#undo-a-reallocation) a [Opakovaně provést opětovné přidělení](#reallocate-multiple-times) dále v tomto článku.

Dolní mřížka na stránce je pojmenována **Řádky**. Když v mřížce **Prodej** vyberete jednu nebo více prodejních objednávek, mřížka **Řádky** zobrazí řádky prodejní objednávky. Vyberte řádky prodejní objednávky, které je třeba opětovně přiřadit. Pokud jste vybrali pouze jednu prodejní objednávku, řádky na totožné prodejní objednávce musejí být znovu přiděleny. K této situaci může dojít, když byl jeden z řádků prodejní objednávky dříve fakturován a poté byl přidán nový řádek, nebo byl odebrán či zrušen existující řádek. Pokud byl řádek odebrán, v mřížce se nezobrazí, a proto jej nelze vybrat. Po spuštění procesu opětovného přidělení však bude stále brán v potaz.

Jakmile vyberete požadované řádky prodejní objednávky, použijte tlačítka v podokně akcí, jak je popsáno zde:

- **Aktualizovat opětovné přidělení** – Vypočet nových částek výnosových cen pro vybrané řádky prodejní objednávky. Pokud byl řádek odstraněn nebo zrušen, opětovné přidělení se provede pouze pro existující řádky, které jste vybrali. Následující obrázek znázorňuje příklad řádků prodejní objednávky před aktualizací opětovného přidělení.

    [![Řádky prodejní objednávky před aktualizací opětovného přidělení](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Nové částky výnosových cen jsou uvedeny ve sloupci **Opětovně přidělená částka** v mřížce **Řádky**. V tomto okamžiku bylo zpracováno opětovné přidělení, ale zatím nebylo vypočítáno. Následující obrázek znázorňuje příklad řádků prodejní objednávky po aktualizaci opětovného přidělení.

    [![Řádky prodejní objednávky po aktualizaci opětovného přidělení](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Zpracovat** – Zpracování nebo zaúčtování opětovně přidělených výnosových cen. Jakmile tohle tlačítko stisknete, opětovné přidělení již nelze vzít zpět. Pokud jste před výběrem tlačítka **Zpracovat** nevybrali možnost **Aktualizovat opětovné přidělení**, opětovné přidělení se spustí automaticky.

    - Pokud nebyl fakturován žádný řádek prodejní objednávky, částky výnosových cen se aktualizují u všech prodejních objednávek, které byly vybrány pro opětovné přidělení.
    - Pokud byl fakturován jeden nebo více řádků prodejní objednávky, zaúčtují se opravné účetní položky a opraví se všechny podrobnosti plánu výnosů, které byly vytvořeny pro řádek fakturované prodejní objednávky.

- **Očekávaný doklad** – Zobrazení náhledu účetních položek, které byly vytvořeny pro všechny fakturované řádky prodejní objednávky. Pokud nebyly fakturovány žádné řádky, nic se nezobrazí. Pokud jste před výběrem tlačítka **Zpracovat** nevybrali možnost **Očekávaný doklad**, opětovné přidělení se spustí automaticky.
- **Opětovné přidělení výnosů** – Otevřete stránku, která zobrazuje přidělení výnosových cen pro všechny vybrané řádky. Žádnou z informací na stránce nemůžete změnit. Stránka zobrazuje částky řádků, které byly použity k opětovnému přidělení.

    [![Částky řádků, které byly použity k opětovnému přidělení](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Obnovit data pro vybraného odběratele** – Pokud byl proces opětovného přidělení spuštěn, ale nebyl dokončen, vymažou se data v tabulce opětovného přidělení pouze pro vybraného odběratele. Příklad: Označíte několik řádků prodejní objednávky, které chcete opětovně přidělit, stránku necháte otevřenou, aniž byste stiskli tlačítko **Zpracovat**, a poté vyprší časový limit stránky. V takovém případě řádky prodejní objednávky zůstanou označeny a nebudou k dispozici jinému uživateli, který by chtěl dokončit proces opětovného přidělení. Stránka může být po otevření dokonce prázdná. V této situaci lze tlačítkem **Obnovit data pro vybraného odběratele** vymazat nezpracované prodejní objednávky, aby mohl proces opětovného přidělení dokončit další uživatel.

## <a name="undo-a-reallocation"></a>Vrátit zpět opětovné přidělení

Opětovné přidělení lze vrátit spuštěním jiného. Opětovné přidělení se provede znovu a uživatel vybere různé řádky prodejní objednávky, které zahrne do druhého procesu opětovného přidělení.

Pokud bylo opětovné přidělení provedeno u dvou nebo více samostatných prodejních objednávek, lze jej vrátit výběrem **Opětovně přidělit cenu pomocí nových řádků objednávky** z jakékoli prodejní objednávky, která je součástí opětovného přidělení. Nemůžete přejít do **Uznání výnosů \> Periodické úkoly \> Opětovně přidělit cenu pomocí nových řádků objednávky** a vrátit zpět opětovné přidělení, protože takto otevřená stránka zobrazuje pouze prodejní objednávky, které nemají žádné ID opětovného přidělení. ID opětovného přidělení je přiřazeno po opětovném přidělení dokumentu.

Na stránce **Opětovně přidělit cenu pomocí nových řádků objednávky** zrušte označení všech prodejních objednávek, které by měly být vyloučeny ze smluvního ujednání. Použijte příslušná tlačítka v podokně Akce, například **Aktualizovat opětovné přidělení** a **Proces** pro zpracování opětovného přidělení. Pokud všechny prodejní objednávky kromě aktivní prodejní objednávky nejsou označeny, ID opětovného přidělení bude při zpracování změny odstraněno.

Pokud bylo opětovné přidělení provedeno přidáním nového řádku k plně nebo částečně fakturované prodejní objednávce, lze jej vrátit zpět pouze odebráním tohoto řádku z prodejní objednávky a dalším spuštěním opětovného přidělení. Řádek prodejní objednávky musí být odstraněn, protože všechny řádky prodejní objednávky jsou považovány za součást stejné smlouvy. Nelze zrušit označení řádku prodejní objednávky, když jste na stránce **Opětovně přidělit cenu pomocí nových řádků objednávky**.

## <a name="reallocate-multiple-times"></a>Opakovaně provést opětovné přidělení

Opakovaná opětovná přidělení proti stejné prodejní objednávce, pokud bylo ve smlouvě provedeno více změn. Každé opětovné přidělení spustí přiřazení ID opětovného přidělení prodejní objednávce nebo skupině prodejních objednávek, aby seskupilo změny. Pokud je provedeno opakované opětovné přidělení, každé další opakované přidělení použije stejné ID opakovaného přidělení jako to první.

Například je zadána prodejní objednávka 00045 a má více řádků. Jakmile je prodejní objednávka plně fakturována, je k ní přidán nový řádek prodejní objednávky. Opětovné přidělení pak spustíte otevřením stránky **Opětovně přidělit cenu pomocí nových řádků objednávky** buď z prodejní objednávky 00045, nebo přechodem na **Uznání výnosů \> Periodické úkoly \> Opětovně přidělit cenu pomocí nových řádků objednávky**. ID opětovného přidělení **Reall000001** je přiřazeno k prodejní objednávce.

Druhá prodejní objednávka, 00052, je vytvořena pro stejnou smlouvu. Opětovné přidělení lze znovu spustit otevřením stránky **Opětovně přidělit cenu pomocí nových řádků objednávky** z prodejní objednávky 00045, ale ne z prodejní objednávky 00052. Pokud otevřete stránku **Opětovně přidělit cenu pomocí nových řádků objednávky** z prodejní objednávky 00052, prodejní objednávka 00045 se nezobrazí, protože jí bylo přiřazeno ID opětovného přidělení. Stránka zobrazuje pouze prodejní objednávky, které nemají žádné ID opětovného přidělení.

Druhé opětovné přidělení lze provést dvěma způsoby. Opětovné přidělení prodejní objednávky 00045 můžete vrátit zpět. V tomto případě bude ID opětovného přidělení odstraněno a poté můžete opětovné přidělení provést buď z prodejní objednávky 00045 nebo z prodejní objednávky 00052. Případně můžete otevřít stránku **Opětovně přidělit cenu pomocí nových řádků objednávky** z prodejní objednávky 00045 a přidat druhou prodejní objednávku. Při zpracování opětovného přidělení bude ID opětovného přidělení **Reall000001** přiřazeno k prodejní objednávce 00045 i k prodejní objednávce 00052.

## <a name="scenarios-for-reallocation"></a>Scénáře, kdy lze použít opětovné přidělení

Následující témata popisují různé scénáře, kdy lze použít uznání výnosů:

- [Opětovné přidělení uznání výnosů – scénář 1](rev-rec-reallocation-scenario-1.md) – Jsou zadány dvě prodejní objednávky, ale ty jsou pouze potvrzeny. K podobným výsledkům dojdete, když jsou potvrzeny více než dvě prodejní objednávky.
- [Opětovné přidělení uznání výnosů – scénář 2](rev-rec-reallocation-scenario-2.md) – Jsou zadány dvě prodejní objednávky a po fakturaci první z nich odběratel přidá položku do smlouvy.
- [Opětovné přidělení uznání výnosů – scénář 3](rev-rec-reallocation-scenario-3.md) – Do existující fakturované prodejní objednávky je přidán nový řádek.
- [Opětovné přidělení uznání výnosů – scénář 4](rev-rec-reallocation-scenario-4.md) – Z existující, částečně fakturované prodejní objednávky je odebrán řádek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
