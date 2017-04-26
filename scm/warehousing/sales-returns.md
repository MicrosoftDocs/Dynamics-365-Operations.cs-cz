---
title: "Prodejní vratky"
description: "Toto téma obsahuje informace o procesu pro vratky. Obsahuje informace o zákazníkovi vrátí a jejich vliv na ocenění a na skladě množství zásob."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Prodejní vratky

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o procesu pro vratky. Obsahuje informace o zákazníkovi vrátí a jejich vliv na ocenění a na skladě množství zásob.

Z různých důvodů mohou zákazníci vrátit zboží. Například položka může být vadný nebo ji nemusí splnit očekávání zákazníka. Spuštění vrácení procesu Pokud zákazník vydá požadavek na vrácení zboží. Poté, co obdržel požadavek zákazníka je vytvořena objednávka vratky v 365 Microsoft Dynamics pro operace.

## <a name="return-order-process"></a>Proces objednávky vratky
Na následujícím obrázku poskytuje přehled procesu objednávky vratky.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

Existují dva typy vratky proces: fyzické vrátit a pouze Dal.

-   **Fyzické navrácení** – objednávka vratky opravňuje fyzické navrácení produktů.
-   **Dal jen** – vratky úvěru odběratele opravňuje však nevyžaduje odběratel fyzicky vrátit produkty.

### <a name="physical-return-order-process"></a>Proces fyzického vratky

1.  **Vytvořte objednávku vratky.** Povolení pro zákazníka vrátit žádné vadné nebo nežádoucí produkty formálně dokumentu. Vratka nevyžaduje, aby společnost přijmout vrácených produktů nebo poskytnout úvěr zákazníka. Pokud je přijat výnos, můžete povolit náhradu zboží dříve, než se vrátil vadné zboží.
2.  **Dorazí na sklad pro kontrolu.** Dokončení počáteční inspekce a ověřování proti dokladu nákupní vratky. Vratka podporuje také karantény vráceného zboží pro další kontrolu a řízení jakosti.
3.  **Určete dispozice.** Dokončení procesu inspekce a rozhodnout, co by mělo být provedeno pomocí vrácených produktů. V rámci tohoto kroku rozhodnete, zda vám bude úvěr zákazníka, odmítnout vrácení produktu, nebo přijmout produkt vrátit, šrot produkt a potom odeslat zákazníkovi náhradní produkt.
4.  **Vygenerování dodacího listu.** Vygenerování dodacího listu a potvrzení rozhodnutí dispozice, které jste provedli v kroku 3. Finalizovat logistické procesy.
5.  **Generování faktury.** Uzavření objednávky vratky.

### <a name="credit-only-process"></a>Pouze proces Dal

1.  **Vytvořte objednávku vratky.** Povolení k zákazníkovi, jemuž Dal bez vrácení vadné nebo nežádoucí produkty formálně dokumentu. **Pouze Dal** dispoziční kód povoluje rozhodnutí o úvěru zákazníka bez fyzické navrácení.
2.  **Generování faktury.** Generovat dobropis a potom zavřete objednávky vratky.

## <a name="return-material-authorization"></a>Povolení návratu materiálu
Zpracování vratek materiál autorizace (RMA) je založena na funkci prodejní objednávky. RMA je registrován jako vratka, který je vytvořen jako prodejní objednávka a mohou mít jiné prodejní objednávky přidruženy, nazvanou objednávky náhrady. Původní číslo RMA propojení obou prodejních objednávek.

-   **Objednávka vratky** – registrace RMA, vytvořte objednávku vratky, což je prodejní objednávky, který má přiřazený typ, **vrácené objednávky.** Všechny změny, které provedete informace vrácené položky je automaticky aktualizováno v prodejní objednávce. Do objednávky vratky se stavem **Open**, se nezobrazí v seznamu prodejních objednávek. Použít vrácené položky pro zpracování doručení a přijetí vráceného zboží, jakož i úvěru pouze dispoziční akce schválit (viz oddíl **dispoziční kódy a dispoziční akce**). Všechny následné procesy musí být zpracován v prodejní objednávce.
-   **Objednávky náhradních** – při objednávky náhrady musí být dodáno zákazníkovi, vrácené položky mohou obsahovat druhý přidružené prodejní objednávky. Můžete ručně vytvořit objednávku náhrady pro vrácené položky pro podporu okamžité dodávky. Případně náhradní objednávky lze vytvářet automaticky po dokončení pro vrácené položky řádku Předmět, který má dispoziční kód, který označuje náhradní doručení, kontrolu a potvrzení. Objednávka náhrady má stejnou funkci, která je spojena s prodejní objednávkou. Například můžete použít ke konfiguraci vlastního produktu jako náhradu zboží, vytvořit výrobní zakázky na hodnotu vrácenou položku opravit, vytvořit nákupní objednávku přímé dodávky zaslat náhradní od dodavatele nebo podporu na jiné účely.

## <a name="create-a-return-order"></a>Vytvořit vratku
Jakmile se zákazník obrátí organizace vrátit vadné nebo nežádoucí produkt a/nebo připisují spuštění procesu objednávky vratky. Po organizaci akceptuje návrat, návrat je doložena objednávky vratky. Tato vratka bude kontaktní místo interní zpracování vráceného produktu. Následující obrázek znázorňuje postup vytvoření objednávky vratky.  

[![Postup pro vytvoření objednávky vratky](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Vytvořit záhlaví objednávky vratky

Při vytvoření objednávky vratky informace v následující tabulce musí být zahrnuta.

| Pole              | popis                                              | Poznámky                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Účet zákazníka   | Odkaz do tabulky Zákazníci                       | Je nutné zadat existující účet odběratele.                                                                                                                                                                                                                                                                                                  |
| Adresa dodání   | Vráceného zboží na adresu                 | Ve výchozím nastavení je použita adresa organizace. Pokud v hlavičce je vybrána konkrétní sklad, dodací adresa se změní na adresu dodání ze skladu. Na tuto adresu můžete změnit **vrátit podrobnosti objednávky** stránky.                                                                                                  |
| Web/sklad     | Web nebo skladu, který přijímá vrácené produkty | Adresa dodání pro objednávku vratky závisí na adresu webu nebo skladu.                                                                                                                                                                                                                                 |
| Číslo RMA         | Identifikátor, který je přiřazen k objednávce vratky              | RMA číslo se používá jako alternativní klíč v celém procesu objednávky vratky. Přiřazené číslo RMA je založen na RMA číselné řady, která je nastavena na **parametry pohledávek** stránky.                                                                                                                              |
| Konečný termín           | Poslední datum, kdy položky mohou být vráceny.               | Výchozí hodnota je vypočítána jako aktuální datum plus dobu platnosti. Například pokud vrácení je platná pouze po dobu 90 dní od data, kdy je vytvořena objednávka vratky a Vratka byla vytvořena dne 1, hodnota v poli je **dne 30**. Doba platnosti je nastavena na **parametry pohledávek** stránky. |
| Kód důvodu vrácení | Jeho důvod vrácení produktu          | Kód příčiny je vybrána v seznamu uživatelem definované kódy. Toto pole můžete kdykoli aktualizovat.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Vytvořit řádky objednávky vratky

Po dokončení vrácení záhlaví vrácené řádky lze vytvořit pomocí jedné z následujících metod:

-   Ručně zadejte podrobnosti položky, množství a další informace pro každý řádek vrácenky.
-   Vytvoření řádku vratky pomocí **najít prodejní objednávku** funkce. Doporučujeme použít tuto funkci, při vytvoření objednávky vratky. **Najít prodejní objednávku** funkce vytvoří z řádku vratky odkaz na řádek vyfakturované prodejní objednávky a načte řádek podrobností, jako je číslo zboží, množství, ceny, slevy a hodnoty nákladů z řádku prodeje. Odkaz pomáhá zaručit, že při vrácení produktu společnosti ji má oceněnou v stejné pořizovací cena aby byla prodávána za. Odkaz také ověří, zda vrátit objednávky nejsou vytvářeny pro množství, které přesahuje množství, které bylo prodáno na faktuře.

**Poznámka:** vrácené řádky, které mají odkaz prodejní objednávky jsou zpracovány jako opravy nebo změny, prodej. Další informace naleznete v části "Post do knihy" dále v tomto tématu.

### <a name="charges"></a>Poplatky

Poplatky mohou být přidány do objednávky vratky prostřednictvím jednoho nebo více z následujících metod:

-   Poplatky můžete ručně přidat do záhlaví objednávky vratky a řádek vratky.
-   Poplatky lze automaticky přidán k hlavičce objednávky vratky jako funkce kód důvodu vrácení.
-   Poplatky lze automaticky přidán na řádek vratky na základě řádku kódu dispozice.

Poplatky jsou automaticky vkládají kód důvodu vrácení nebo dispoziční kód je přiřazen k řádku. Pokud je později změnit kód důvodu, nebude odebrána existující vstupní poplatek, ale mohou být přidány nové položky nákladů, založené na nový kód důvodu. Přidáte-li náklady na řádky vratky, poplatky, které se vypočítávají jako procentní podíl hodnoty řádku nebo pořadí záporný, když řádek nebo řádek objednávky negativní, pokud je procento je také záporné číslo. Poplatek, který má zápornou hodnotu představuje úvěr zákazníka.

### <a name="return-reason-codes"></a>Kódy důvodů vrácení

Použitím kódů důvodu vrátí, může pomoci usnadnit návrat vzorků k analýze. Kódy důvodu poskytují informace o proč chce zákazník vrátit zboží. Některé organizace mají mnoho kódů příčiny. Tyto organizace mohou seskupit kódy příčiny do skupiny kódů důvodů získat lepší přehled a pro souhrnné hlášení.

### <a name="disposition-codes-and-disposition-actions"></a>Dispoziční kódy a dispoziční akce

Důležitým krokem v procesu objednávky vratky je přiřazení dispoziční kód, který řádek vratky jako součást registrace doručení. Dispoziční kód určuje následující informace:

-   **Finanční důsledky** – by měly zákazníka připsána za vrácené zboží a řádek vratky by měly být přidány žádné poplatky?
-   **Dispozice vráceného zboží,** – by měly být položky můžete přidat zpět do zásob, by měly být zlikvidovány nebo by měla být zákazníkovi vrácena?
-   **Logistické vráceného zboží,** – Zákazník by měly být vydávány náhradní zboží?

Kromě určení, jak jsou odstraněny vráceného zboží, může způsobit dispoziční kódy nákladů pro řádek vrácenky. Můžete také používají k seskupení vrátí pro statistickou analýzu. Dispoziční kódy jsou definovány jako část instalace vratek. Nicméně každý kód dispozice musí odkazovat vestavěné dispoziční akce. Následující tabulka obsahuje vestavěné dispoziční kódy a jejich akce. **Důležité:** Pokud by neměla vrátit položku, ale stále musí být připsány zákazníka, přiřadit **pouze Dal** dispoziční kód na řádku vratky.

<table>
<thead>
<tr class="header">
<th>Dispoziční kód</th>
<th>Finanční dopady</th>
<th>Důsledky pro logistiku</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pouze Dal</td>
<td><ul>
<li>Zákazníkovi je účtováno ve prospěch prodejní cena mínus žádné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení položky je zaúčtována do hlavní knihy.</li>
</ul></td>
<td>Položka nesmí vrácena. Tato akce dispozice se používá v následujících případech:
<ul>
<li>Existuje dostatek důvěry mezi stranami.</li>
<li>Náklady spojené s vrácením vadného zboží je nepřiměřeně vysoká.</li>
<li>Položky nelze povolit zpět do zásob. Z jiných důvodů není nutné fyzické navrácení.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreditní</td>
<td><ul>
<li>Zákazníkovi je účtováno ve prospěch prodejní cena mínus žádné poplatky nebo náklady.</li>
<li>Hodnota zásob zvýšením ceny vráceného zboží.</li>
</ul></td>
<td>Položka bude vrácena a je přidána zpět do zásob.</td>
</tr>
<tr class="odd">
<td>Nahradit a připsat na stranu Dal</td>
<td><ul>
<li>Zákazníkovi je účtováno ve prospěch prodejní cena mínus žádné poplatky nebo náklady.</li>
<li>Hodnota zásob zvýšením ceny vráceného zboží.</li>
<li>Samostatné prodejní objednávky pro náhradu je vytvořena a je zpracována samostatně.</li>
</ul></td>
<td>Položka bude vrácena a je přidána zpět do zásob.</td>
</tr>
<tr class="even">
<td>Nahradit a vyřadit</td>
<td><ul>
<li>Zákazníkovi je účtováno ve prospěch prodejní cena snížená o žádné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení položky je zaúčtována do hlavní knihy.</li>
<li>Samostatné prodejní objednávky pro náhradu je vytvořena a je zpracována samostatně.</li>
</ul></td>
<td>Položka je vrácena a zlikvidován.</td>
</tr>
<tr class="odd">
<td>Vrátit odběrateli</td>
<td>Žádný, s výjimkou jakékoli poplatky nebo poplatky.</td>
<td>Položka bude vrácena, ale je zaslána zákazníkovi po prohlídce. Tato akce dispozice lze použít pokud položka byla záměrně poškozena nebo záruky byl zrušen.</td>
</tr>
<tr class="even">
<td>Odpad</td>
<td><ul>
<li>Zákazníkovi je účtováno ve prospěch prodejní cena mínus žádné poplatky nebo náklady.</li>
<li>Ztráta z vyřazení položky je zaúčtována do hlavní knihy.</li>
</ul></td>
<td>Zboží je vráceno nebo zlikvidován.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Příchodu na sklad pro kontrolu
Před zaúčtováním dodacího listu fyzicky příjmem vrácené zboží do zásob, položky musí projít registrace příchodu a volitelné kontroly. Na následujícím obrázku poskytuje přehled procesu doručení. Následující oddíly popisují jednotlivé kroky, které je znázorněno na obrázku.  

[![Proces doručení](./media/salesreturn03.png)](./media/salesreturn03.png)  

Proces má několik variant, které nejsou zahrnuty v tomto tématu. Zde jsou některé z těchto variant:

-   Nepoužívejte **přehled doručení** seznamu a vytvořte deník doručení. Ručně vytvořte deník doručení. Vrácení objednávky, bude mít **prodeje** jako odkaz.
-   Pokud používáte řízení skladu, generování palet. Vrácené řádek bude mít stav **doručeno** během přepravy palet.
-   Zaregistrovat pomocí přijetí vráceného zboží přímo z řádku objednávky vratky **registrace** funkce.

Během procesu doručení vrátí integrována obecný postup pro přijetí na sklad. Proces doručení také podporuje vytváření karanténní příkazy pro vrácené zboží, které musí být podrobeno samostatné kontroly.

### <a name="identify-products-in-the-arrival-overview-list"></a>Identifikaci produktů v seznamu přehled doručení

**Přehled doručení** stránky jsou uvedeny všechny plánované doručení příchozích. **Poznámka:** doručení z vratky musí být zpracovány odděleně od ostatních typů transakcí příjezdu. Po označenou příchozí balíček na **přehled doručení** stránky (například pomocí průvodního dokladu RMA), v podokně akcí, klepněte na tlačítko **zahájit doručení** k vytvoření a inicializace deník doručení, který odpovídá příjezdu.

### <a name="edit-the-arrival-journal"></a>Upravit deník doručení

Nastavením **řízení karantény** možnosti **Ano**, můžete vytvořit karanténní příkaz na řádku vratky. Pokud řádek byl odeslán do karantény pro inspekci, nelze zadat dispoziční kód. **Poznámka:** Pokud nastavíte **řízení karantény** možnost na **Ano** do skupiny skladových modelů položky, **řízení karantény** možnost na **řádky deníku** stránky bude označena na řádku deníku doručení a nemůže být změněn. Pokud řádek odeslán do karantény, je nutné zadat příslušný karanténní sklad. Pokud řádek doručení není odeslána ke kontrole, musí pracovník skladu příjezdu zadat dispoziční kód přímo na řádku deníku doručení a poté zaúčtovat deník doručení. Pokud je stejný kód dispozice neměla být přiřazena celé množství řádku vratky nebo neobdržel úplné množství na řádku, je nutné rozdělit řádek. Při rozdělení řádku deníku doručení rozdělíte řádek vrácenky (**SalesLine**) a vytvořit nové ID šarže. Snížíte množství v řádku deníku doručení lze rozdělit řádek. Při zaúčtování deníku je vytvořen nový řádek vratky, který má stav **očekávané** pro zbývající množství. Můžete také rozdělit řádek klepnutím na **funkce**&gt;**rozdělení**.

### <a name="process-the-quarantine-order"></a>Procesu karanténní příkaz

Pokud vrácené produkty jsou odeslány ke kontrole v karanténním skladu, se v karanténní příkaz doplní jakékoli další zpracování. Jeden karanténní příkaz je vytvořen pro každý řádek vstupu, který je odeslán do karantény. Dispoziční kód označuje výsledek procesu kontroly. Karanténní příkaz můžete rozdělit, stejně jako deník doručení můžete rozdělit. Rozdělení karanténního příkazu způsobit odpovídající rozdělení řádku vratky. Po zadání kódu dispozice dokončit karanténní příkaz pomocí buď **konec** funkce nebo **hlášení jako dokončené** funkce. Vyberete-li **hlášení jako dokončené**, je vytvořen nový příjezdu do určeného skladu. Pak můžete zpracovat toto doručení pomocí **přehled doručení** stránky. Pokud doručení pochází z karanténního příkazu, nemůžete změnit dispoziční kód, který je přiřazen během inspekce. Pokud dokončení karanténního příkazu pomocí **konec** funkce šarže je automaticky zaregistrován. Položky v některých případech může být odeslána zpět z karantény dodávky a příjmu na oddělení. Inspektor karantény, například nemusí znát umístění k uložení zboží ve skladu. Odpovídající dodací list v tomto případě musí být aktualizovány správně zaregistrovat a působit na dispoziční kód, který je určen z důvodu karantény. Při registraci řádku vratky, můžete zákazníkovi odesláno potvrzení o přijetí. **Potvrzení vratky** se podobá sestavě dokladu nákupní vratky. **Potvrzení vratky** sestavy není zapsány do deníku nebo jinak zaregistrována v systému a není povinný krok v procesu objednávky vratky.

## <a name="replace-a-product"></a>Nahradit produktem
Existují dvě metody pro správu produktu náhradní:

-   **Předem náhradní** – nahradit produkt před přijetí vráceného produktu od zákazníka.
-   **Nahrazením dispoziční kód** – automaticky vytvořte nový řádek objednávky náhrady.

### <a name="up-front-replacement"></a>Předem provedená náhrada

V předem náhradní náhradu zboží můžete doručit zákazníkovi před položka je vrácena. Tato metoda je užitečná, pokud je položka například částí stroje, které nelze odebrat, pokud je k dispozici jeho proběhne náhradní díl, nebo pokud chcete mít co nejdříve náhradní produkt zákazníkovi. Objednávky předem náhrady je nezávislé prodejní objednávky. Informace v záhlaví je inicializován od zákazníka a informace o řádku je inicializována z objednávky vratky. Úprava, zpracování a odstranit objednávku náhrady nezávisle na objednávku vratky. Při odstranění objednávky náhrady zpráva, že pořadí byl vytvořen jako objednávka náhrady. Následující obrázek znázorňuje proces náhrady předem.  

[![Předem náhradní proces](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Objednávka vratky obsahuje odkaz na objednávku náhrady. Pokud pro objednávku vratky je vytvořena objednávka předem náhradní, před vrácení vadné položky, nelze vybrat dispoziční kódy pro náhradní po vrácení vadné zboží.

### <a name="replacement-by-disposition-code"></a>Nahrazení kódu dispozice

Pokud dodáváte zákazníkovi náhradní zboží a použijete **nahradit a vyřadit** nebo **nahradit a Dal** dispoziční akce v objednávce vratky pomocí procesu, který je zobrazen na následujícím obrázku.  

[![Náhradní proces při použití kódu dispozice](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Náhradu zboží budou doručeny pomocí nezávislé prodejní objednávky, prodejní objednávky náhradního. Tato prodejní objednávka je vytvořena při vygenerování dodacího listu pro objednávku vratky. Záhlaví objednávky používá informace od zákazníka, který je odkazován v hlavičce objednávky vratky. Informace o řádku jsou shromažďovány z informací zadaných na **náhradu zboží** stránky. **Náhradu zboží** stránky musí být vyplněno pro řádky, které mají dispoziční akce, které začínají slovo "replace". Nicméně množství ani totožnost náhradu zboží je ověřeno nebo omezené. Toto chování umožňuje pro případy, kdy zákazník požaduje stejné zboží, ale v jiné konfigurace nebo velikost a také případy, kde zákazník chce úplně jinou položku. Ve výchozím nastavení, zadání shodné zboží **náhradu zboží** stránky. Můžete však vybrat jiné položky, za předpokladu, že byla nastavena funkce. **Poznámka:** můžete upravit a odstranit prodejní objednávky náhradního po jeho vytvoření.

## <a name="generate-a-packing-slip"></a>Vygenerování dodacího listu
Před vrácené zboží lze přijímat do zásob, je nutné aktualizovat dodací list objednávky, které položky patří do. Stejně jako proces aktualizace faktury je aktualizace finanční transakce, dodacího listu aktualizace fyzické aktualizaci zásob záznamu je proces. Jinými slovy tento proces potvrdí změny zásob. V případě vrátí, kroky, které jsou přiřazeny akce dispozice jsou implementovány při balení aktualizaci. Při generování dodacího listu, dojde k následujícím událostem:

-   Ve skladu standardní proces slouží k provádění fyzického příjmu. Zaúčtování do hlavní knihy jsou generovány, jestliže skupiny modelu skladu (**Zaúčtovat fyzické zásoby**) a parametry pohledávek (**Zaúčtovat dodací list do hl**) jsou nastaveny správně.
-   Vyřazené položky, které byly označeny pomocí dispoziční akce, který obsahuje slovo "odpad" a skladová ztráta je zaúčtována do hlavní knihy.
-   Položky, které byly označené **vrátit zákazníkovi** dispoziční akce jsou přijata a dodány odběrateli. Tyto položky mít žádný čistý efekt na skladě.
-   Je vytvořena prodejní objednávku. Tato prodejní objednávka je na základě informací na **náhradu zboží** stránky.

Můžete generovat pouze pro řádky, které mají stav vrácení dodacího listu **registrované**a pouze pro celé množství na řádku vratky. Pokud máte několik řádků v objednávce vratky **registrované** stav, můžete generovat dodací list pro podmnožinu řádků odstraněním řádků z **Zaúčtovat dodací list** stránky. Jsou definována v částečné vrátí řádky objednávky vratky, ne co se týče dodávek vratky. Proto pokud obdržíte celé množství, která je uvedena na jednom řádku vratky, ale nic obdržíte od ostatních řádků v objednávce vratky, dodání není částečné dodání. Pokud řádek vratky vyžaduje 10 jednotek zboží vrátit, ale zobrazuje pouze čtyři jednotky, je doručení však částečné dodání. Není-li očekávané vrácené zboží dorazilo, jste vyňaté z dodávky a počkejte, zbytek vrácené množství k doručení. Alternativně můžete zaregistrovat a zaúčtovat částečné množství. Jako součást procesu zaúčtování dodacích listů můžete přiřadit referenční číslo dodacího listu ze zákazníka dodací doklady s řádky objednávky. Toto přidružení je nepovinný a je pouze pro referenci. Avšak nevytvoří žádné transakční aktualizace. Obecně můžete přeskočit dodacího listu procesu a přejít přímo k fakturaci. Kroky, které byste provedli během dodacího listu generace v tomto případě proběhne při fakturaci.

## <a name="generate-an-invoice"></a>Generovat fakturu
I když **objednávka vratky** stránka obsahuje informace a akce, které jsou nutné pro zpracování zvláštní logistické aspekty objednávky vratky, je nutné použít **prodejní objednávka** stránky dokončete proces fakturace. Vaše organizace může pak faktury vratky a prodejní objednávky současně a stejná osoba může dokončit proces fakturace podle potřeby. Chcete-li zobrazit vratky z **prodejní objednávka** stránky, klikněte na odkaz pro otevření přidružené prodejní objednávky číslo prodejní objednávky. Objednávka vratky můžete najít také na **všechny prodejní objednávky** stránky. Vrácení objednávky jsou prodejní objednávky, které mají typ objednávky z **vrácené objednávky**.

### <a name="credit-correction"></a>Úvěrové vyrovnání

Jako součást procesu fakturace ověřte správnost všech vedlejších nákladů. Způsobit zaúčtování hlavní knihy se opravy (Storno), zvažte použití **Dal korekce** možnost na **jiné** karty **zaúčtování faktury** stránky při zaúčtování faktury nebo dobropisu. **Poznámka:** ve výchozím nastavení, **Dal korekce** Pokud je aktivovaná možnost **dobropis jako oprava** možnost na **parametry pohledávek** stránku povolen. Doporučujeme však, že vám nebude účtovat vrátí Storno.

## <a name="create-intercompany-return-orders"></a>Vytvoření mezipodnikových objednávek vratek
Objednávky vratky můžete dokončit mezi dvěma společnostmi v rámci organizace. Podporovány jsou následující scénáře:

-   Jednoduchý mezipodnikové vrátí mezi dvěma společnostmi, které se účastní mezipodnikových vztahů
-   Mezipodnikový řetězec, který je vytvořen při vytvoření objednávky vratky zákazníka v prodejní společnosti
-   Mezipodnikový řetězec, který je vytvořen při vytvoření objednávky vratky dodavateli v kupující společnosti
-   Vrátí přímé doručení dodávky mezi externím zákazníkům a dvou společností, které se účastní mezipodnikových vztahů

### <a name="setup"></a>Nastavení

Na následujícím obrázku minimální nastavení, které jsou vyžadovány pro dvě společnosti účastní mezipodnikových vztahů a využívat mezipodnikový obchod.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

V následujícím scénáři CompBuy je kupující společnosti a CompSell je prodávající společnosti. Obvykle prodávající společnost dodává zboží kupující společnosti nebo, v případech dodávky Přímá dodávka přímo ke koncovému zákazníkovi. V CompBuy, Mezipodnikového dodavatele\_CompSell je definován jako mezipodnikový koncový bod, který je spojen s firmou CompSell. Současně v CompSell mezipodnikové odběratele\_CompBuy je definován jako mezipodnikový koncový bod, který je spojen s firmou CompBuy. V obou společnostech musí být definovány podrobnosti zásad příslušné akce a mapování hodnot. V případě dodávky Přímá dodávka je vytvořen mezipodnikové objednávky vratky, která je také mezipodnikové prodejní objednávky v prodejní společnosti. RMA číslo mezipodnikové vratky lze vydat z pořadového čísla RMA v CompSell, nebo může být zkopírován z RMA čísla přiřazená původní objednávky vratky v CompBuy. Nastavení čísla RMA na **nákupní požadavek** tyto akce určit zásady akce v CompBuy. Pokud se synchronizuje číslo RMA, byste měli naplánovat číslo střetům riziko v případě, že obě společnosti používají stejnou číselnou řadu.

### <a name="simple-intercompany-returns"></a>Jednoduchý mezipodnikové vrátí

Tento scénář zahrnuje dva podniky ve stejné organizaci, jak je znázorněno na následujícím obrázku.  

[![Jednoduché vrácení mezipodnikové](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Při vytvoření objednávky vratky dodavateli v kupující společnosti nebo vytvoření objednávky vratky zákazníka v prodejní společnosti lze vytvořit řetězce objednávek. Dynamics 365 pro operace vytvoří odpovídající objednávky v jiné společnosti a zajišťuje, že záhlaví a řádek informace o dodavateli vrátit odráží pořadí, že objednávka vratky nastavení u zákazníka. Objednávka vratky, které je vytvořeno můžete zahrnout nebo vyloučit odkaz (**najít prodejní objednávku**) do existující faktury odběratele. Dodacích listů a faktur dvě objednávky budou zpracovány jednotlivě. Například není nutné generovat dodacího listu pro objednávku vratky dodavateli před vytvořením dodacího listu pro objednávku vratky zákazníka.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Vrátí přímé doručení dodávky mezi třemi stranami

Tento scénář lze vytvořit, pokud předchozí prodej **přímé dodávky** typu dokončení a pokud faktury proti zákazníka existuje ve společnosti, který spolupracuje se zákazníkem. Na následujícím obrázku má společnost CompBuy dříve prodané a fakturované produkty zákazníkovi Extern. Produkty přímo od společnosti CompSell dodáno zákazníkovi prostřednictvím mezipodnikový řetězec.  

[![Vrátí přímé doručení dodávky mezi třemi stranami](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Pokud externí zákazník chce vrátit produkty, objednávky vratky (RMA02) je vytvořen pro odběratele ve společnosti CompBuy. Pokud chcete vytvořit mezipodnikový řetězec, musí být označeny objednávku vratky pro přímou dodávku. Při použití **najít prodejní objednávku** funkce vyberte fakturu odběratele, který chcete vrátit, usazen mezipodnikový řetězec, který se skládá z následujících dokladů:

-   **Původní objednávka vratky:** RMA02 (společnost CompBuy)
-   **Nákupní objednávka:** PO02 (společnost CompBuy)
-   **Mezipodnikové objednávky vratky:** RMA\_00032 (firma CompSell)

Po vytvoření řetězu mezipodnikové přímé dodávky všechny fyzické manipulaci a zpracování údajů musí dojít v rámci mezipodnikové objednávky vratky, RMA\_00032 ve společnosti CompSell. Produkty, nemůže být přijato ve společnosti CompBuy. Pokud je přiřazen kód dispozice mezipodnikové vratky, je synchronizován s původní objednávku vratky, aby bylo umožněno řádné fakturace původní objednávky.

## <a name="post-to-the-ledger"></a>Zaúčtování do hlavní knihy
Zaúčtování do knihy, které jsou generovány při fakturaci objednávky vratky jsou ovlivněny několik důležitých nastavení a parametry:

-   **Náklady na vrácení** – pro skladové modely jiné než **standardní náklady**, **nákladová cena vrácení** parametr určuje cenu zboží, pokud byl přijat zpět do zásob nebo zlikvidován. Pro výpočet správné ocenění zásob, je důležité, abyste nastavili **nákladová cena vrácení** parametr správně. Použijete-li **najít prodejní objednávku** funkce, chcete-li vytvořit řádek vratky, který obsahuje odkaz na fakturu odběratele, **nákladová cena vrácení** hodnota je shodná s nákladovou cenou zboží, které prodává. Jinak hodnota nákladové ceny vycházejí z nastavení položky nebo lze zadat ručně.
-   **Korekce/Storno Dal** – **Dal korekce** parametr **zaúčtování faktury** stránky určuje, zda účtování má nahrané jako kladné položky (MD/d) nebo jako oprava, negativní položky.

V následujících příkladech je reprezentována náklady na vrácení **fakturační cenu**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Příklad 1: Objednávka vratky neodkazuje faktury odběratele

Vratka neodkazuje na faktuře zákazníka. Vrácené zboží je účtováno ve prospěch. **Dal korekce** při generování faktury pro objednávku vratky nebo dobropis, není vybrán parametr.  

[![Vratka neodkazuje invoic zákazníka](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Poznámka:** hlavní cena zboží se používá jako výchozí hodnota pro **nákladová cena vrácení** parametr. Výchozí ceny se liší od nákladová cena v době vydání zásob. Důsledkem tedy vznikly ztráty 3. Navíc neobsahuje objednávku vratky slevy, která byla poskytnuta zákazníkovi na prodejní objednávku. Proto dochází k nadměrnému Dal.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Příklad 2: Úvěrové vyrovnání je vybrána pro objednávku vratky

Příklad 2 je stejný jako v příkladu 1, ale **Dal korekce** je vybrán parametr při generování faktury pro objednávku vratky.  

[![Kde je vybráno storna objednávky vratky](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Poznámka:** účetní zápisy hlavní knihy, které jsou zadány jako záporné opravy.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Příklad 3: Řádek vratky je vytvořen pomocí funkce Najít prodejní objednávku

V tomto příkladu je vytvořen řádek vratky pomocí **najít prodejní objednávku** funkce. **Dal korekce** parametr není vybrán při vytvoření faktury.  

[![Vrátí řádek objednávky, který je vytvořen pomocí najít prodejní objednávku.](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Poznámka:****slevy** a **nákladová cena vrácení** jsou správně nastaveny. Proto dojde k stornování faktury odběratele.




