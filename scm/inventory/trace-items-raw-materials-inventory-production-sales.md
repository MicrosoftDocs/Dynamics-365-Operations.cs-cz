---
title: "Sledování zboží a surovin ve skladu, při výrobě a prodeji"
description: "Toto téma popisuje, jak můžete použít sledování položky k identifikaci, kde bylo použito zboží nebo suroviny, nebo kde budou použity ve výrobě a prodejních procesech."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c901dfa448a320d447b43dd5ab80417229f388b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Sledování zboží a surovin ve skladu, při výrobě a prodeji

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak můžete použít sledování položky k identifikaci, kde bylo použito zboží nebo suroviny, nebo kde budou použity ve výrobě a prodejních procesech. 

Funkce sledování položky je k dispozici na stránce **Sledování položky**. Následující části popisují, jak můžete používat sledování položky, a jaké jsou možnosti a omezení.

## <a name="what-is-item-tracing"></a>Co je sledování položky?
Sledování položky je nástroj business intelligence (BI), který poskytuje přehled o zdroji a cíli zboží a surovin v daném dodavatelsko-odběratelském řetězci. Výrobci mohou sledovat zboží, suroviny nebo přísady zpět k dodavateli a předávat je do výroby a prodej hotového výrobku. Sledování položky umožňuje výrobcům jednat v souladu s předpisy a pomáhá také úředníkům pro kvalitu a vedoucím výroby analyzovat a provést akci vedoucí k řešení odchylek v kvalitě výrobků a materiálů. Následují některé příklady postupů, které může výrobce použít pro sledování položky:

-   Určení množství zboží nebo surovin, které je aktuálně ve skladu a kde je uloženo.
-   Určení, jaké množství zboží nebo surovin bylo vyexpedováno a kterým odběratelům bylo expedováno.
-   Určení jakýchkoli plánovaných dodávek zboží nebo surovin.
-   Vyhledejte výrobní zakázky, které používají zboží nebo suroviny a jsou plánované, probíhající nebo hlášené jako dokončené.
-   Zjistěte, kde bylo zboží nebo suroviny zakoupeny.
-   Zjistěte, kde bylo zboží nebo suroviny spotřebovány ve výrobě jiné položky.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Co lze sledovat a existují omezení?
Můžete sledovat historické skladové transakce pro položky a suroviny podle čísla položky a sledovací dimenze, jako je sériové číslo, číslo dávky nebo číslo dávky pro dodavatele. Pokud zboží nebo surovina nemá přiřazenou sledovací dimenzi, nelze je sledovat. Vzhledem k tomu, že sledování je založeno na skladových transakcích, existují při sledování položek určitá omezení. Existují například omezení týkající se transakcí pro projekty, dlouhodobý majetek a maloobchod. Kromě toho jsou v podrobnostech o sledování uvedeny společné produkty, ale nejsou zahrnuty vedlejší produkty. Sledování zahrnuje všechny transakce skladu z jednoho místa na druhé. Uživatelé proto mohou být množstvím informací zahlceni. Sledování je zobrazeno vždy pro jednu právnickou osobu současně. V mezipodnikovém kontextu neexistují žádné schopnosti využitelné mezi více společnostmi. Pro každou společnost, kde jsou položky přijaté nebo vydané, je nutné spustit nové sledování.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Jaká kritéria lze určit pro sledování položky?
Kritéria, která jsou požadována pro sledování položky, jsou: číslo položky, sledovací dimenze, například číslo dávky nebo sériové číslo a směr. Následující tabulka popisuje kritéria, která můžete použít při sledování položky.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skupina polí</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Číslo zboží</td>
<td>Zadejte identifikátor pro zboží nebo suroviny, které sledujete.</td>
</tr>
<tr class="even">
<td>Dimenze produktu</td>
<td>Volitelné: Sledujte specifické aspekty definice výrobků, jako je například konfigurace, velikost, barva nebo styl.</td>
</tr>
<tr class="odd">
<td>Sledovací dimenze</td>
<td>Zadejte číslo dávky, číslo dávky dodavatele nebo sledovací dimenze sériového čísla. Použijete-jako kritérium číslo dávky, pokud tuto informaci zaznamenáte, zobrazí se číslo dávky dodavatele.</td>
</tr>
<tr class="even">
<td>Dimenze úložiště</td>
<td>Volitelné: Sledujte položky, které byly uloženy v určitém místě.</td>
</tr>
<tr class="odd">
<td>Období</td>
<td>Volitelné: Zadejte data k omezení sledování na konkrétní období. Podrobnosti o sledování zobrazí pouze dokumenty a transakce, které byly vytvořeny mezi těmito daty.</td>
</tr>
<tr class="even">
<td>Dopředu nebo dozadu</td>
<td>Vyberte směr sledování. Můžete řadit dopředu nebo dozadu:
<ul>
<li><strong>Dozadu</strong> – Sledování směrem dolů k identifikaci zdroje, množství, které zbývá na skladě a jakýchkoli výrobních zakázek, které jsou alespoň částečně nahlášeny jako dokončené.</li>
<li><strong>Vpřed</strong> – Sledování směrem nahoru k identifikaci místa určení. Můžete vyhledávat prodejní objednávky a zákazníky, kterým byla sledovaná položka nebo surovina alespoň částečně dodána.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Jaké informace jsou uvedeny v podrobnostech o sledování?
Výsledky sledování se zobrazují v chronologickém pořadí na pevné záložce **Podrobnosti** na stránce **Sledování položky**. Pořadí se liší v závislosti na směru sledování. Podrobnosti zahrnují všechny transakce nákupu zboží od dodavatele k prodeji položky odběrateli. Výsledky sledování zahrnují i dočasné produkty, které se vztahují k položce nebo dimenzi sledování zadaným v kritériích sledování. Nejvyšší uzel ukazuje množství zboží ve skladové jednotce, které zbude na skladě podle dimenzí uskladnění, které byly zadány v kritériích sledování. **Poznámka:** Podrobností o sledování se snímkem informací, které byly k dispozici při sledování byla provedena. Podrobnosti o sledování nebudou aktualizovány, pokud se informace o změně po provedení sledování změní.

## <a name="why-dont-some-nodes-contain-any-details"></a>Proč některé uzly neobsahují žádné podrobnosti?
Aby se snížilo množství informací v podrobnostech o sledování, pouze uzel pro první výskyt zboží nebo surovin obsahuje podrobnosti. Pokud vybraný uzel neobsahuje podrobné informace, můžete zobrazit uzel, který podrobnosti obsahuje, kliknutím na **Přejít na sledovaný řádek**. Kliknutím na **Přejít zpět** se můžete vrátit na původní uzel.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Je možné zobrazit pouze určitý typ dokumentu? Mužů například zobrazit pouze výrobní zakázky, odběratele nebo dodavatele?
Ano, můžete otevřít stránky seznamu, které obsahují pouze určitý typ dokumentu nebo transakce, z podrobností o sledování. Tyto stránky lze otevřít pomocí položky nabídky **Sledování** v podokně akcí ve skupinách **Položka**, **Prodej**, **Nákup**, **Výroba** a **Kvalita**. Například pro zobrazení seznamu dodavatelů v podrobnostech o sledování klikněte na **Sledování** &gt; **Nákup** &gt; **Dodavatelé**. Stránky se seznamy uvádějí souhrn dokumentů nebo transakcí z podrobností o sledování. Stránky se seznamem **Čekající transakce**, **Nevyřízené objednávky** a **Prodejní objednávky** za neexpedované zboží obsahují také jiné informace, které nejsou zahrnuty v podrobnostech o sledování. Kromě toho vždy zobrazují výsledky k aktuálnímu datu bez ohledu na to, byl zadán rozsah kalendářních dat. V následující tabulce jsou popsány další podrobnosti, které tyto stránky mohou obsahovat.

| Seznamy                    | Popis                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prodejní objednávky za neexpedované zboží | Zobrazte řádky prodejní objednávky, které nebyly vyskladněny, a nezobrazí se tedy v podrobnostech o sledování.                                                                                                                                                                                                                        |
| Čekající objednávky           | Zobrazte všechny čekající výrobní zakázky pro sledovanou položku, bez ohledu na sledovací dimenze, které byly použity v kritériích sledování. Můžete také zobrazit čekající výrobní zakázky, kde je sledovaná položka některou přísadou a kde nebyly provedeny žádné registrace a žádné transakce nejsou hlášeny jako dokončené pro objednávku. |
| Čekající transakce     | Zobrazte čekající skladové transakce pro sledované zboží, které zahrnuje zadané dimenze sledování nebo prázdnou sledovací dimenzi. V podrobnostech o sledování můžete také zobrazit kombinace čekajících skladových transakcí pro položky a sledovací dimenze nebo prázdnou hodnotu.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Kolik úrovní je možné sledovat nahoru nebo dolů v kusovník nebo receptuře?
V kusovnících nebo receptuře lze sledovat jednu úroveň nahoru nebo dolů. Pokud například spustíte sledování surovin, můžete si prohlédnou hotový výrobek a vedlejší produkty. Pokud však sledujete vedlejší produkt, nebudou podrobnosti o sledování zahrnovat hotový produkt.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Jak lze zobrazit další informace o dokumentu nebo transakci v podrobnostech o sledování?
Na pevné záložce **Podrobnosti** můžete zobrazit další informace o vybraném dokumentu nebo transakci v podrobnostech o sledování následujícími dvěma způsoby:

-   Při výběru uzlu v podrobnostech o sledování na pevné záložce **Podrobnosti** se na ostatních záložkách s náhledem na stránce zobrazují informace o dokumentu nebo transakci v uzlu.
-   Stránku s podrobnostmi o dokumentu můžete otevřít ve vybraném uzlu otevřít klepnutím na tlačítko **Zobrazit podrobnosti**. Například pokud vyberete uzel, který popisuje výrobní zakázky a kliknete na tlačítko **Zobrazit podrobnosti**, zobrazí se stránka s podrobnostmi **Výrobní zakázky**.

Některé pevné záložky poskytují přístup k dalším informacím o vybraném uzlu. Na pevné záložce **Neshody** můžete například zjistit, zda existuje historie neshody, kliknutím na **Dotazy**. Na pevné záložce **Dávka** můžete kliknutím na **Seznam skladu** zobrazit množství fyzických zásob, které jsou právě na skladě, a všech skladových transakcí, které zahrnují dávku.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Lze spustit sledování více než jedno sledování a poté porovnat podrobnosti?
Po spuštění sledování, můžete pomocí možností tlačítka **Sledovat z uzlu** spustit nové sledování transakcí ve vybraném uzlu:

-   **Dozadu** nebo **Vpřed** – spuštění nového sledování pro vybraný uzel a přepis podrobností o sledování pro aktuální sledování.
-   **Nové zpětné sledování** nebo **Nové dopředné sledování** – spuštění nového sledování v novém okně a ponechání podrobností o aktuálním sledování.

Pokud chcete použít možnost **Nové zpětné sledování** nebo **Nové dopředné sledování**, musíte použít funkci **Otevřít v novém okně** a nové sledování tak otevřít v novém okně.

## <a name="can-i-save-the-trace-details"></a>Je možné uložit podrobnosti o sledování?
Informace můžete uložit na kartu **Podrobnosti** jako soubor XML kliknutím na **Export** pod akcí ****Sledování**** na panelu akcí. Kromě podrobností o sledování obsahuje soubor XML kritéria sledování, nadřazený uzel a množství na skladě. Možnost uložení podrobností o sledování je užitečné, například pokud mají být připojeny informace o objednávce kvality nebo jiná dokumentace o kompatibilitě. Můžete určit, kde je soubor uložen. Chcete-li zobrazit soubor ihned, vyberte možnost **Zobrazit dokument**. **Poznámka:** Soubor se uloží vždy, i v případě, že ho chcete pouze zobrazit. Ve výchozím nastavení se otevře soubor XML v okně prohlížeče. To lze změnit klepnutím pravým tlačítkem myši na soubor, výběrem volby **Otevřít v programu** a potom výběrem programu, který se má použít k zobrazení obsahu.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Lze vypočítat zůstatek pro konkrétní položku nebo látku?
Informace můžete exportovat ze souhrnných stránek do aplikace Microsoft Excel. Otevřete odpovídající stránku, klepněte na ikonu **Otevřít v aplikaci Microsoft Office** a poté vyberte **Exportovat do aplikace Excel**. Tato funkce je zvlášť užitečná, když chcete vypočítat hromadný zůstatek položky nebo látky ze stránky **Souhrnné transakce**. Na stránce **Souhrnné transakce** můžete filtrovat podle zboží nebo složky a dávky, pokud chcete, a poté exportovat informace do aplikace Excel. V aplikaci Excel například můžete izolovat množství na skladě, prodané množství a částku, která byla použita ve výrobě.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Můžu zjistit, zda existuje historie problémů se zbožím nebo surovinami?
Podrobnosti o sledování zahrnují informace o objednávkách kvality a neshodách, které zahrnují zboží nebo suroviny. Souhrn objednávek kvality a neshod lze zobrazit klepnutím na **Objednávka kvality** nebo **Neshody** v podokně akcí. **Poznámka:** Destruktivní objednávky kvality se mohou v podrobnostech o sledování zobrazit více než jednou. Při vytvoření destruktivní objednávky kvality pro dokument, například nákupní objednávky, se zobrazí pro každou transakci pro daný dokument.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Existují nějaké možnosti pro vytváření sestav souvisejících se sledováním položky?
Můžete vygenerovat sestavu **Expedováno odběratelům** k identifikaci množství zboží nebo surovin, které bylo dodáno, a zákazníků, kterým byl expedován. Pro vytvoření dotazu vztahujícího se ke kompatibilitě lze generovat sestavu pro všechny odběratele. Pro vytvoření dotazu vztahujícího se na služby zákazníkům lze generovat sestavu pro vybraného odběratele. Pokud produkt představovaly suroviny, které byly použity při výrobě dokončené položky, bude zahrnuta také dokončená položka. **Poznámka:** Pokud používáte funkce pro odstranění nebo archivaci prodejních objednávek, budou výsledky sestavy také zahrnovat všechny prodejní objednávky, které byly odstraněny nebo archivovány.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Je možné sledovat souběžné a vedlejší produkty?
Souběžné produkty lze sledovat, ale není možné sledovat vedlejší produkty, protože k nim nejsou obvykle přiřazeny sledovací dimenze. Když sledujete zboží, budou jakékoli související souběžné produkty zahrnuty do podrobností o sledování. Uzel, který obsahuje souběžný produkt, má v podrobnosti slovo "souběžný produkt". Podrobnosti o souběžném produktu můžete z obrazit také výběrem uzlu v podrobnostech o sledování a kliknutím na pevnou záložku **Výroba**.




