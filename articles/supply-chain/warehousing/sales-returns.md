---
title: "Prodejní vratky"
description: "Toto téma obsahuje informace o procesu pro vratky. Obsahuje informace o zboží vraceném zákazníkem a o vlivu vracení na oceňování a na skladové množství zásob."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fa56911c19e9b6514829084221ba03c7cd421c92
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="sales-returns"></a>Prodejní vratky

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o procesu pro vratky. Obsahuje informace o zboží vraceném zákazníkem a o vlivu vracení na oceňování a na skladové množství zásob.

Zákazníci mohou zboží vracet z různých důvodů. Například může být nějaký kus zboží vadný nebo může nesplňovat očekávání zákazníka. Proces vracení začíná tím, když zákazník vydá požadavek na vrácení zboží. Po obdržení požadavku zákazníka je v aplikaci Microsoft Dynamics 365 for Finance and Operations vytvořena objednávka vrácení.

## <a name="return-order-process"></a>Proces objednávky vrácení
Následující obrázek podává přehled procesu objednávky vrácení.  

[![Proces objednávky vrácení](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Existují dva typy procesu vracení: fyzické vrácení a jen kredit.

-   **Fyzické vrácení** – objednávka vrácení opravňuje fyzické navrácení produktů.
-   **Pouze Dal** – Objednávka vrácení opravňuje kredit odběratele, avšak nevyžaduje, aby odběratel produkty fyzicky navrátil.

### <a name="physical-return-order-process"></a>Proces objednávky fyzického vrácení

1.  **Vytvořit objednávku vrácení.** Formálně zdokumentovat povolení zákazníkovi vrátit jakékoli vadné nebo nežádoucí produkty. Objednávka vrácení nevyžaduje, aby společnost vrácené produkty přijala ani aby zákazníkovi vydala náhradu platby. Pokud bude vrácení přijato, můžete schválit odeslání náhradního zboží dříve, než bude vráceno vadné zboží.
2.  **Dorazí na sklad pro kontrolu.** Dokončit prvotní inspekce a ověřování oproti dokladu o objednáce vrácení. Objednávka vrácení podporuje také karantény vráceného zboží pro další kontrolu a řízení jakosti.
3.  **Určete dispozici.** Dokončení procesu inspekce a rozhodnutí, co by mělo být provedeno s vrácenými produkty. V rámci tohoto kroku rozhodnete, zda vrátíte peníze zákazníkovi, odmítnete vrácení produktu, nebo zda přijmete vrácení produktu, zlikvidujete produkt a odešlete zákazníkovi náhradní produkt.
4.  **Vytvořit dodací list.** Vytváření dodacího listu a potvrzení rozhodnutí dispozice, které jste provedli v kroku 3. Finalizovat logistické procesy.
5.  **Vytvořit fakturu.** Uzavřít objednávku vrácení.

### <a name="credit-only-process"></a>Proces pouze připisující kredit

1.  **Vytvořit objednávku vrácení.** Formálně zdokumentovat povolení zákazníkovi obdržet vrácení platby, aniž by vracel vadné nebo nežádoucí produkty. Dispoziční kód **Jen kredit** povoluje rozhodnutí o úhradě zákazníkovi bez fyzického vrácení.
2.  **Vytvořit fakturu.** Vytvořte dobropis a potom zavřete objednávku vrácení.

## <a name="return-material-authorization"></a>Schválení vrácených materiálů
Zpracování schvalování vracených materiálů (RMA) je založeno na funkci prodejní objednávky. RMA je registrována jako objednávka vracení, která je vytvořena jako prodejní objednávka, a může mít k sobě přidruženu jinou prodejní objednávku zvanou objednávka náhrady. Obě prodejní obědnávky odkazují na číslo RMA, které je původcem.

-   **Objednávka vrácení** – Chcete-li zaregistrovat RMA, můžete vytvořit objednávku vrácení, což je prodejní objednávka, která má přiřazen typ. **Vrácená objednávka.** Všechny změny, které provedete na informacích o RMA, budou automaticky aktualizovány v prodejní objednávce. Dokud objednávka vrácení nebude mít stav **Open**, nebude se zobrazovat v seznamu prodejních objednávek. RMA používáte ke zpracování příchodů a přijímání vraceného zboží, jakož i ke schvalování dispoziční akce spočívající pouze v připsání kreditu (viz oddíl **Dispoziční kódy a dispoziční akce**). Všechny ostatní následné procesy musejí být zpracovány v prodejní objednávce.
-   **Náhradní objednávka** – Když bude třeba odeslat zákazníkovi objednávku náhrady, může RMA obsahovat druhou přidruženou prodejní objednávku. Pro podporu okamžitého zaslání můžete ručně vytvořit objednávku náhrady pro RMA. Případně lze náhradní objednávku vytvořit automaticky po dokončení příchodu, prohlídky a převzetí pro položku řádku RMA, která má dispoziční kód označující náhradu. Objednávka náhrady má stejnou funkci, jaká je spojena s prodejní objednávkou. Například ji můžete použít ke konfiguraci vlastního produktu jako náhradního zboží, k vytvoření výrobní zakázky na opravu vráceného zboží, vytvoření nákupní objednávky přímé dodávky za účelem zaslání náhrady od dodavatele, nebo na podporu jiných účelů.

## <a name="create-a-return-order"></a>Vytvořit vratku
Proces objednávky vrácení začíná, když zákazník kontaktuje Vaši organizaci s vrácením vadného nebo nebo nežádoucího produktu a/nebo s nárokem na vracení platby. Poté, co Vaše organizace vrácení přijme, bude vrácení zdokumentováno formou objednávky vrácení. Tato objednávka vrácení bude ústředním bodem interního zpracování vraceného produktu. Následující obrázek znázorňuje postup vytvoření objednávky vrácení.  

[![Postup pro vytvoření objednávky vrácení](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Vytvořit hlavičku objednávky vrácení

Při vytváření objednávky vrácení je třeba zahrnout informace z následující tabulky.

| Pole              | popis                                              | Poznámky                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Účet zákazníka   | Odkaz na tabulku zákazníka                       | Musíte zadat existující účet odběratele.                                                                                                                                                                                                                                                                                                  |
| Adresa dodání   | Adresa, na kterou je zboží vraceno.                 | Ve výchozím nastavení je použita adresa organizace. Pokud je v hlavičce je vybrán konkrétní sklad, dodací adresa se změní na dodací adresu skladu. Tuto adresu můžete změnit na stránce **Podrobnosti objednávky vrácení**.                                                                                                  |
| Místo/sklad     | Místo nebo sklad, který má vrácený produkt přijmout | Adresa dodání pro objednávku vrácení se určuje podle dodací adresy místa nebo skladu.                                                                                                                                                                                                                                 |
| Číslo RMA         | ID, které bylo přiřazeno objednávce vrácení              | Číslo RMA se v celém procesu objednávky vrácení používá jako alternativní klíč. Identifikační číslo, které je přiřazeno, se zakládá na číselné řadě nastavené na stránce **Parametry pohledávek**.                                                                                                                              |
| Konečný termín           | Poslední datum, kdy bude lze zboží vrátit.               | Výchozí hodnota se počítá jako aktuální datum plus doba platnosti. Například pokud vrácení je platné pouze po dobu 90 dní od data, kdy je byla vytvořena objednávka vrácení a objednávka vrácení byla vytvořena dne 1. května, hodnota v poli je **30. června**. Doba platnosti se nastavuje na stránce **parametry pohledávky**. |
| Kód důvodu vrácení | Důvody vrácení zboží uvedené odběratelem          | Kód příčiny se vybírá v seznamu uživatelem definovaných kódů důvodů. Toto pole můžete kdykoli aktualizovat.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Vytvořit řádky objednávky vrácení

Po dokončení záhlaví vrácení můžete vytvořit řádky vrácení pomocí jedné z následujících metod:

-   Ručně zadejte údaje o zboží, množství a další informace pro každý řádek vrácení.
-   Vytvoření řádku objednávky vrácení pomocí funkce **Najít prodejní objednávku**. Při vytváření objednávky vrácení doporučujeme používat tuto funkci. Funkce **Najít prodejní objednávku** založí odkaz z řádku objednávky vrácení na řádek vyfakturované prodejní objednávky a načte údaje řádku, jako například číslo zboží, množství, a hodnoty ceny, slevy a nákladů z řádku prodeje. Odkaz pomáhá zaručit, aby byl produkt po svém vrácení společnosti oceněn na stejnou hodnotu za jednotkové množství, za jakou byl prodáván. Odkaz také ověří, zda nejsou vytvořeny objednávky vracení pro množství přesahující množství prodané podle faktury.

**Poznámka:** Řádky objednávky vrácení, které mají odkaz na prodejní objednávku, jsou zpracovány jako opravy nebo změny prodeje. Další informace naleznete v části „Zařazení do hlavní knihy“ dále v tomto tématu.

### <a name="charges"></a>Poplatky

Poplatky a změny lze přidat do objednávky vracení prostřednictvím jedné nebo více následujících metod:

-   Poplatky můžete ručně přidávat do záhlaví objednávky vrácení, do řádku objednávky vrácení, nebo do obojího.
-   Poplatky lze automaticky přidávat k hlavičce objednávky vrácení jako funkci kódu důvodu vrácení.
-   Poplatky lze automaticky přidávat k řádku objednávky vrácení na základě dispozičního kódu řádku.

Poplatky se automaticky přidávají po přidělení kódu důvodu vrácení nebo dispozičního kódu danému řádku. Pokud je později změněn kód důvodu, nebude odebrána existující položka poplatku, ale může být přidána nová položka poplatku na základě nového kódu důvodu. Přidáte-li na řádky objednávky vrácení poplatky, pak poplatky, které se vypočítávají jako procentní podíl hodnoty řádku nebo objednávky se stanou zápornými, když budou řádek nebo objednávka řádku záporné, nebude-li procento také záporným číslem. Poplatek, který má zápornou hodnotu, představuje dobropis pro zákazníka.

### <a name="return-reason-codes"></a>Kódy důvodů vrácení

Použitím kódů důvodů na objednávky vracení můžete napomoci usnadnit analýzu vzorů vracení. Kódy důvodů poskytují informace o tom, proč chce zákazník vrátit nějaké zboží. Některé organizace mají mnoho kódů důvodů. Tyto organizace mohou seskupit kódy důvodů do skupin kódů důvodů za účelem získání lepšího přehledu a pro souhrnné hlášení.

### <a name="disposition-codes-and-disposition-actions"></a>Dispoziční kódy a dispoziční akce

Důležitým krokem v procesu objednávky vrácení je přiřazení dispozičního kódu k řádku objednávky vrácení v rámci registrace doručení. Dispoziční kód určuje následující informace:

-   **Finanční důsledky** – Měla by zákazníkovi být připsána částka za vrácené zboží a měly by být přičteny nějaké poplatky k řádku objednávky vrácení?
-   **Dispozice vráceného zboží,** – Mělo by být zboží přidáno zpět do zásob, mělo by být zlikvidováno, nebo by mělo být vráceno zákazníkovi?
-   **Logistika vráceného zboží,** – Mělo by být zákazníkovi vydáno náhradní zboží?

Kromě určení toho, co bude provedeno s vráceným zbožím, mohou dispoziční kódy přivodit účtování poplatků na řádku objednávky vrácení. Lze je také použít k seskupení vracení pro statistickou analýzu. Dispoziční kódy jsou definovány v rámci konfigurace objednávek vracení. Nicméně každý kód dispozice musí odkazovat na jednu z integrovaných dispozičních akcí. Následující tabulka uvádí integrované dispoziční kódy a jejich akce. **Důležité:** Kdyby nějaké zboží nebylo vráceno, ale zákazníkovi by i tak bylo potřeba připsat částku k dobru, přiřaďte řádku objednávky vrácení dispoziční kód **Jen kredit**.

<table>
<thead>
<tr class="header">
<th>Dispoziční kód</th>
<th>Finanční důsledky</th>
<th>Důsledky pro logistiku</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pouze Dal</td>
<td><ul>
<li>Zákazníkovi je připsána ve prospěch prodejní cena mínus veškeré případné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení zboží je zaúčtována do hlavní knihy.</li>
</ul></td>
<td>Položka by neměla být vracena. Tato dispoziční akce se používá v následujících případech:
<ul>
<li>Existuje dostatek důvěry mezi stranami.</li>
<li>Náklady spojené s vrácením vadného zboží jsou nepřiměřeně vysoké.</li>
<li>Zboží nelze povolit zpět do zásob. Z důvodů jiných podmínek není nutné fyzické navrácení.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditní</td>
<td><ul>
<li>Zákazníkovi je připsána ve prospěch prodejní cena mínus veškeré případné poplatky nebo náklady.</li>
<li>Hodnota zásob se zvyšuje o hodnotu vráceného zboží.</li>
</ul></td>
<td>Zboží bude vráceno a bude přidáno zpět do zásob.</td>
</tr>
<tr class="odd">
<td>Nahradit a připsat na stranu Dal</td>
<td><ul>
<li>Zákazníkovi je připsána ve prospěch prodejní cena mínus veškeré případné poplatky nebo náklady.</li>
<li>Hodnota zásob se zvyšuje o hodnotu vráceného zboží.</li>
<li>Pro náhradu bude vytvořena a samostatně zpracována samostatná prodejní objednávka.</li>
</ul></td>
<td>Zboží bude vráceno a bude přidáno zpět do zásob.</td>
</tr>
<tr class="even">
<td>Nahradit a vyřadit</td>
<td><ul>
<li>Zákazníkovi bude připsána ve prospěch prodejní cena mínus veškeré případné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení zboží je zaúčtována do hlavní knihy.</li>
<li>Pro náhradu bude vytvořena a samostatně zpracována samostatná prodejní objednávka.</li>
</ul></td>
<td>Zboží je vráceno a zlikvidováno.</td>
</tr>
<tr class="odd">
<td>Vrátit odběrateli</td>
<td>Žádné, vyjma případných poplatků nebo nákladů.</td>
<td>Zboží je vráceno, ale po prohlídce je zasláno zpět zákazníkovi. Tuto dispoziční akci lze použít, pokud bylo zboží svévolně poškozeno nebo pokud zanikla platnost záruky.</td>
</tr>
<tr class="even">
<td>Odpad</td>
<td><ul>
<li>Zákazníkovi je připsána ve prospěch prodejní cena mínus veškeré případné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení zboží je zaúčtována do hlavní knihy.</li>
</ul></td>
<td>Zboží je vráceno nebo zlikvidováno.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Příchod do skladu na prohlídku
Než budete moci fyzicky přijmout vrácené zboží do zásob vydáním průvodky, musí zboží absolvovat registraci a případnou prohlídku na příchodu. Následující ilustrace podává přehled procesu příchodu. Následující oddíly popisují jednotlivé kroky, které jsou znázorněny na obrázku.  

[![Proces doručení](./media/salesreturn03.png)](./media/salesreturn03.png)  

Proces má několik jiných variant, které nejsou probírány v tomto tématu. Zde je několik příkladů těchto variant:

-   Při vytváření Deníku doručení nepoužívejte seznam **Přehled doručení**. Namísto toho ručně vytvořte deník doručení. Objednávky vrácení budou mít jako odkaz **Prodejní objednávku**.
-   Jestliže používáte řízení skladu, vytvořte přepravy palet. Řádek vrácení bude mít během přepravy palet stav **Doručeno**.
-   Pomocí funkce **Registrace** zaregistrujte přijetí vráceného zboží přímo z řádku objednávky.

Během procesu příchodu budou vrácení integrována s obecným postupem pro přijetí na sklad. Proces příchodu také podporuje vytváření karanténních příkazů pro vrácené zboží, které musí být podrobeno samostatné kontrole.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identifikujte produkty v seznamu přehled příchodů

Na stránce **Přehled příchodů** jsou uvedeny všechna plánovaná doručení příchodů. **Poznámka:** Doručení z objednávek vrácení musí být zpracováno odděleně od ostatních typů transakcí příchodů. Po identifikaci příchozího balíčku na stránce **přehled doručení** (například pomocí průvodního dokladu RMA) v podokně akcí klikněte na tlačítko **Zahájit příchod** k vytvoření a inicializaci deníku příchodů, který bude odpovídat danému příchodu.

### <a name="edit-the-arrival-journal"></a>Upravte deník příchodů.

Nastavením možnosti **Řízení karantény** na **Ano** můžete vytvořit karanténní příkaz pro řádek objednávky vrácení. Pokud byl řádek odeslán do karantény k inspekci, nemůžete zadat dispoziční kód. **Poznámka:** Jestliže nastavíte možnost **Řízení karantény** ve skupině skladových modelů položky na **Ano**, pak možnost **Řízení karantény** na stránce **řádky deníku** bude označena pro řádek deníku příchodů a nebude možno ji změnit. Když bude řádek odeslán do karantény, budete muset zadat příslušný karanténní sklad. Pokud řádek doručení není odeslán ke kontrole, musí pracovník skladu příjezdu zadat dispoziční kód přímo na řádek deníku doručení a poté zaúčtovat deník doručení. Jestliže stejný kód dispozice nemá být přiřazen celému množství řádku objednávky vrácení nebo jestliže nebylo obdrženo plné množství řádku, je nutné rozdělit řádek. Při rozdělení řádku deníku příchodů rozdělíte také řádek objednávky vrácení (**Řádek prodejů**) a vytvoříte nové ID šarže. Řádek můžete rozdělit také snížením množství na řádku deníku doručení. Při zaúčtování deníku je vytvořen nový řádek objednávky vrácení, který má stav **Očekávaný** pro zbývající množství. Řádek můžete také rozdělit kliknutím na **Funkce** &gt; **Rozdělit**.

### <a name="process-the-quarantine-order"></a>Proces karanténního příkazu

Jestliže budou vrácené produkty odeslány ke kontrole do karanténního skladu, veškeré další zpracování bude dokončeno v karanténní objednávce. Pro každý řádek vstupu odesílaný do karantény je vytvořen jeden karanténní příkaz. Dispoziční kód označuje výsledek procesu kontroly. Karanténní příkaz můžete rozdělit, stejně jako můžete rozdělit deník příchodů. Jestliže rozdělíte karanténní příkaz, způsobíte tím odpovídající rozdělení řádku objednávky vrácení. Po zadání kódu dispozice dokončete karanténní příkaz pomocí buďto funkce **Konec** nebo funkce **Nahlásit jako dokončené**. Vyberete-li **Nahlásit jako dokončené**, bude vytvořen nový příchod do určeného skladu. Pak můžete tento příchod zpracovat pomocí stránky **Přehled příchodů**. Jestliže příchod pochází z karanténního příkazu, nemůžete změnit dispoziční kód, který byl přiřazen při inspekci. Pokud karanténní příkaz dokončíte pomocí funkce **konec** funkce šarže bude automaticky zaregistrována. V některých případech může být zboží odesláno zpět z karantény na oddělení dodávek a příjmů. Inspektor karantény například nemusí vědět, kam má být zboží ve skladu uloženo. V tomto případě musí být aktualizován příslušný dodací list , by bylo možno řádně zaregistrovat a jednat podle uvedeného dispozičního kódu z důvodu karantény. Při registraci řádku vracení lze zákazníkovi zaslat potvrzení přijetí. Hlášení o **Potvrzení vrácení** se podobá dokladu objednávky vrácení. Hlášení o **Potvrzení vrácení** se nezapisuje do deníku ani jinak neregistruje do systému a není povinným krokem v procesu objednávky vrácení.

## <a name="replace-a-product"></a>Nahradit produkt
Existují dvě metody pro správu náhradního produktu:

-   **Náhrada předem** – Nahradit produkt před přijetím vráceného produktu od zákazníka.
-   **Nahrazení podle dispozičního kódu** – Automaticky vytvořte nový řádek objednávky náhrady.

### <a name="up-front-replacement"></a>Předem provedená náhrada

Při náhradě předem lze náhradu zboží doručit zákazníkovi už předtím, než bude zboží vráceno. Tato metoda je užitečná například tehdy, jestliže je toto zboží součástí stroje, kterou nelze vyjmout, není-li k dispozici náhradní díl namísto něj, nebo jestliže chcete, aby Váš zákazník měl náhradní produkt k dispozici co nejdříve. Objednávka náhrady předem je nezávislá prodejní objednávka. Informace v záhlaví jsou inicializovány od zákazníka a informace o řádku jsou inicializovány z objednávky vrácení. Objednávku náhrady můžete upravovat, zpracovávat a odstraňovat nezávisle na objednávce vracení. Při výmazu objednávky náhrady obdržíte zprávu, že objednávka byla vytvořena jako objednávka náhrady. Následující obrázek znázorňuje proces náhrady předem.  

![Proces náhrady předem](./media/SalesReturn04.png)

Objednávka vrácení obsahuje odkaz na objednávku vrácení. Pokud pro objednávku vrácení bude už před vrácením vadného zboží vytvořena objednávka předem, pak po vrácení vadného zboží už nemůžete vybrat dispoziční kódy pro náhradu.

### <a name="replacement-by-disposition-code"></a>Náhrada podle dispoičního kódu

Pokud dodáváte zákazníkovi náhradní zboží a v objednávce vrácení použijete dispoziční akce **Nahradit a vyřadit** nebo **Nahradit a připsat na účet** postupujte podle procesu vyobrazeného na následujícím obrázku.  

![Náhradní proces při použití dispozičního kódu](./media/SalesReturn05.png)

Náhradní zboží bude doručeno pomocí nezávislé prodejní objednávky, náhradní prodejní objednávky. Tato prodejní objednávka je vytvářena při generování dodacího listu pro objednávku vrácení. Záhlaví objednávky používá informace od zákazníka, na které je odkazováno v hlavičce objednávky vrácení. Informace o řádku jsou shromažďovány z informací zadaných na stránce **Náhrada zboží**. Stránka **Náhrada zboží** musí být vyplněna pro řádky, které mají dispoziční akce, které začínají slovem "replace" ("nahradit"). Avšak ani množství ani totožnost náhradního zboží nebude ověřena ani omezena. Toto chování umožňuje případy, kdy zákazník požaduje stejné zboží, ale v jiné konfiguraci nebo velikosti a také případy, kdy zákazník chce úplně jiné zboží. Dle výchozího nastavení se shodné zboží zadává na stránce **náhrada zboží**. Můžete však vybrat jiné zboží, za předpokladu, že byla nastavena funkce. **Poznámka:** náhradní prodejní objednávku můžete po jejím vytvoření upravit enbo vymazat.

## <a name="generate-a-packing-slip"></a>Vytvořte dodací list
Před přijetím vrácených položek na sklad musíte aktualizovat dodací list pro objednávku, do které toto zboží náleží. Stejně jako je proces aktualizace faktury aktualizací finanční transakce, proces aktualizace dodacího listu je fyzickou aktualizací skladového záznamu. Jinými slovy, tento proces potvrdí změny zásob. V případě vrácení jsou kroky přiřazené k dispoziční akci implementovány v průběhu aktualizace dodacího listu. Při generování dodacího listu dojde k následujícím událostem:

-   Ve skladu je k provádění fyzického příjmu používán standardní proces. Zaúčtování do hlavní knihy jsou generována tehdy, jestliže je správně nastavena skupina modelu skladu (**Zaúčtovat fyzické zásoby**) a parametry pohledávek (**Zaúčtovat dodací list do hlavní knihy**).
-   Položky, které byly označeny pomocí dispoziční akce obsahující slovo "likvidace" budou zlikvidovány a skladová ztráta bude zaúčtována do hlavní knihy.
-   Položky, které byly označeny dispoziční akcí **Vrátit zákazníkovi** budou přijaty a dodány odběrateli. Tyto položky nemají žádný čistý efekt na inventář.
-   Bude vytvořena nová prodejní objednávka. Tato prodejní objednávka se zakládá na informacích na stránce **náhrada zboží**.

Dodací list můžete vygenerovat pouze pro řádky, které mají stav vrácení dodacího listu **Registrovaný** a to pouze pro plné množství na řádku vrácení. Pokud má několik řádků na objednávce vrácení stav **Registrovaný**, můžete vygenerovat dodací list pro podmnožinu řádků odstraněním řádků ze stránky **Zaúčtovat dodací list**. Částečné dodávky jsou definovány v souvislosti s řádky objednávky vrácení, nikoli v souvislosti s odesláním objednávky vrácení. Pokud tedy obdržíte úplné množství uvedené na jednom řádku objednávky vrácení, ale nic z jiných řádků objednávky vrácení, pak tato dodávka není částečnou dodávkou. Pokud však řádek objednávky vrácení vyžaduje vrácení například deseti jednotek konkrétní položky, ale obdržíte pouze čtyři jednotky, pak jde o částečnou dodávku. Jestliže ne všechno očekávané vracené zboží dorazilo, můžete zásilku odložit stranou a vyčkat na příchod ostatku vráceného množství. Alternativně můžete zaregistrovat a zaúčtovat částečné množství. V rámci procesu účtování dodacích listů můžete volitelně přiřadit referenční číslo dodacího listu z přepravních dokumentů odběratele k řádkům objednávky. Toto přiřazení je nepovinné a má pouze informativní charakter. Nevytváří žádné aktualizace transakcí. Obecně můžete proces dodacího listu přeskočit a přejít přímo k fakturaci. Kroky, které byste provedli při generování dodacího listu, v tomto případě proběhnou při fakturaci.

## <a name="generate-an-invoice"></a>Generovat fakturu
I když stránka **Objednávka vrácení** obsahuje informace a akce, které jsou potřebné pro zpracování zvláštních logistických aspektů objednávky vracení, k dokončení procesu fakturace je nutné použít stránku **Prodejní objednávka**. Vaše organizace může pak fakturovat objednávky vrácení a prodejní objednávky současně a stejná osoba může proces fakturace podle potřeby dokončit. Chcete-li zobrazit objednávkky vracení ze stránky **Prodejní objednávka**, klikněte na odkaz na číslo prodejní objednávky, aby byla otevřena příslušná prodejní onbjednávka. Objednávku vrácení můžete najít také na stránce **Všechny prodejní objednávky**. Objednávky vrácení jsou prodejní objednávky, které mají typ objednávky **Vrácená objednávka**.

### <a name="credit-correction"></a>Úvěrové vyrovnání

V rámci procesu fakturace ověřte správnost veškerých různých nákladů. Aby se ze zaúčtování hlavní knihy staly opravy (Storno), zvažte použití možnosti **Korekce přípisu** na kartě **Ostatní** na stránce **Odeslání faktury** při zaúčtování faktury nebo dobropisu. **Poznámka:** Dle výchozího nastavení bude volba **Korekce přípisu** aktivována tehdy, jestliže byla povolena možnost **Dobropis jako oprava** na stránce **Parametry pohledávek**. Doporučujeme Vám však neúčtovat vrácení se Stornem.

## <a name="create-intercompany-return-orders"></a>Vytvořit mezipodnikové objednávky vrácení
Objednávky vrácení lze dokončit mezi dvěma společnostmi v rámci organizace. Podporovány jsou následující scénáře:

-   Jednoduché mezipodnikové vracení mezi dvěma společnostmi, které se účastní mezipodnikového vztahu
-   Mezipodnikový řetězec, který je vytvořen při vytváření objednávky vracení zákazníka v prodejní společnosti
-   Mezipodnikový řetězec, který je vytvářen při vytváření objednávky vrácení prodejci v kupující společnosti
-   Vrácení přímého doručení dodávky mezi externím zákazníkem a dvěma společnostmi, které se účastní mezipodnikových vztahů

### <a name="setup"></a>Nastavení

Na následujícím obrázku je zobrazeno minimální nastavení, které je potřebné pro dvě společnosti, aby se mohly účastnit mezipodnikových vztahů a využívat mezipodnikový obchod.  

![Minimální nastavení](./media/SalesReturn06.png)

V následujícím scénáři je CompBuy kupující společnost a CompSell je prodávající společnost. Prodávající společnost obvykle dodává zboží buďto kupující společnosti, nebo, v případech scénáře přímé dodávky, přímo ke koncovému zákazníkovi. V CompBuy je mezipodnikový dodavatel\_CompSell definován jako mezipodnikový koncový bod, který je spojen s firmou CompSell. Zároveň je v CompSell je mezipodnikový odběratel\_CompBuy definován jako mezipodnikový koncový bod, který je propojen s firmou CompBuy. V obou společnostech musí být definovány příslušné podrobnosti zásad akce a mapování hodnot. V případě scénáře přímé dodávky zásilky je v prodávající společnosti vytvořena mezipodniková objednávka vrácení, což je také mezipodniková prodejní objednávka. Číslo RMA mezipodnikové objednávky vrácení lze vybrat z posloupnosti čísel RMA v CompSell nebo jej lze zkopírovat z čísla RMA přiřazeného k původní objednávce vrácení v CompBuy. Tyto akce určuje nastavení čísla RMA v zásadách akce **Nákupní požadavek** v CompBuy. Bude-li číslo RMA synchronizováno, měli byste naplánovat zmírňování rizika střetu čísel pro případ, že obě společnosti použijí stejnou číselnou posloupnost.

### <a name="simple-intercompany-returns"></a>Jednoduché mezipodnikové vracení

Tento scénář zahrnuje dva podniky ve stejné organizaci, jak je znázorněno na následujícím obrázku.  

![Jednoduché mezipodnikové vrácení](./media/SalesReturn07.png)

Řetězec objednávky lze založit tehdy, když bude v kupující společnosti vytvořena objednávka vrácení dodavateli nebo když bude v prodávající společnosti vytvořena objednávka vrácení zákazníkovi. Finance and Operations vytvoří příslušnou objednávku v opačné společnosti a zajistí, aby informace hlavičky a řádku na objednávce vrácení dodavateli reflektovaly nastavení na objednávce vrácení zákazníkovi. Objednávka vrácení, která je zavedena, může obsahovat nebo vylučovat referenci (**Najít objednávku vrácení**) na stávající zákaznickou fakturu. Dodací listy a faktury obou objednávek lze zpracovat individuálně. Například není nutné generovat dodací list pro objednávku vrácení dodavateli před vytvořením dodacího listu pro objednávku vrácení zákazníkovi.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Vrácení zásilky přímé dodávky mezi třema stranami

Tento scénář lze založit, jestliže byl dokončen předchozí prodej typu **Přímá dodávka** a jestliže existuje faktura oproti zákazníkovi ve společnosti, která spolupracuje se zákazníkem. Na následujícím obrázku společnost CompBuy nejprve prodala a fakturovala produkty zákazníkovi Extern. Produkty byly zaslány přímo od společnosti CompSell zákazníkovi prostřednictvím mezipodnikového řetězce.  

![Vrácení zásilky přímé dodávky mezi třemi stranami](./media/SalesReturn08.png)

Jestliže chce externí zákazník produkty vrátit, bude vytvořena objednávka vrácení(RMA02) pro odběratele ve společnosti CompBuy. Jestliže chcete vytvořit mezipodnikový řetězec, musí být objednávka vrácení označena pro přímou dodávku. Při použití funkce **Najít prodejní objednávku** vyberte fakturu odběratele, kterou chcete vrátit, a bude založen mezipodnikový řetězec skládající se z následujících dokladů:

-   **Původní objednávka vrácení:** RMA02 (společnost CompBuy)
-   **Nákupní objednávka:** PO02 (společnost CompBuy)
-   **Mezipodniková objednávka vrácení:** RMA\_00032 (společnost CompSell)

Po vytvoření řetězce mezipodnikové přímé dodávky musí veškerá fyzická manipulace s údaji a jejich zpracování probíhat v rámci mezipodnikové objednávky vrácení, RMA\_00032 ve společnosti CompSell. Produkty nemohou být ve společnosti CompBuy přijaty. Pokud je mezipodnikové objednávce vrácení přiřazen kód dispozice, je synchronizována s původní objednávkou vrácení, aby byla umožněna řádná fakturace původní objednávky.

## <a name="post-to-the-ledger"></a>Zaúčtovat do hlavní knihy
Zaúčtování do hlavní knihy, která budou vygenerována při fakturaci objednávky vrácení, budou ovlivněna několika důležitými nastaveními a parametry:

-   **Náklady na vrácení** – pro skladové modely jiné než **Standardní náklady**, **Cena nákladů na vrácení** parametr určuje cenu zboží, když je přijímáno zpět do zásob nebo likvidováno. Pro výpočet správného oceňování zásob je důležité, abyste správně nastavili parametr **Cena nákladů na vrácení**. Použijete-li funkci **Najít prodejní objednávku** k vytvoření řádku objednávky vrácení, který obsahuje odkaz na fakturu odběratele, bude hodnota **Cena nákladů na vrácení** shodná s nákladovou cenou prodávaného zboží. Jinak bude hodnota nákladové ceny vycházet z konfigurace zboží nebo ji lze zadat ručně.
-   **Korekce přípisu nebo storna** – Parametr **Korekce přípisu** na stránce **Zaúčtování faktury** určuje, zda má být zaúčtování zaznamenáno jako kladné položky (MD/D) nebo jako opravné záporné položky.

V následujících příkladech je cena nákladů na vrácení reprezentována jako **fakturační nákladová cena**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Příklad 1: Objednávka vrácení neodkazuje na fakturu odběratele

Objednávka vrácení neodkazuje na fakturu odběratele. Vrácené zboží je účtováno ve prospěch. Při generování faktury pro objednávku vrácení nebo dobropisu není vybrán parametr **Korekce přípisu**.  

![Objednávka vrácení neodkazuje na fakturu odběratele.](./media/SalesReturn09.png)  

**Poznámka:** hlavní cena zboží se používá jako výchozí hodnota pro parametr **Nákladová cena vrácení**. Implicitní cena se liší od nákladové ceny v době vydání zásob. Důsledkem tedy je, že vznikla ztráta 3. Kromě toho objednávka vrácení neobsahuje slevu, která byla poskytnuta zákazníkovi na prodejní objednávku. Proto dojde k přeplatku.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Příklad 2: Pro objednávku vrácení byla vybrána korekce přípisu

Příklad 2 je stejný jako v příkladu 1, ale při generování faktury pro objednávku vrácení je vybrán parametr **Korekce přípisu**.  

![Objednávka vrácení, v níž byla vybrána korekce na straně Dal ](./media/SalesReturn10.png)  

**Poznámka:** Účetní zápisy hlavní knihy jsou zadány jako záporné opravy.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Příklad 3: Řádek objednávky vrácení je vytvořen pomocí funkce Najít prodejní objednávku

V tomto příkladu je řádek objednávky vrácení vytvořen pomocí funkce **Najít prodejní objednávku**. Při vytváření faktury není vybrán parametr **Korekce přípisu**.  

![Řádek objednávky vrácení vytvořen pomocí funkce Najít prodejní objednávku ](./media/SalesReturn11.png)  

**Poznámka:** **Slevy** a **Nákladová cena vrácení** jsou správně nastaveny. Proto dojde k přesnému vzetí zpět faktury odběratele.




