---
title: Plány údržby
description: Toto téma popisuje plány údržby v modulu Správa majetku.
author: johanhoffmann
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectType, EntAssetCounterType, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 143b9337dc9ca530383575e0f9bb16e4313ce96b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839600"
---
# <a name="maintenance-plans"></a>Plány údržby

[!include [banner](../../includes/banner.md)]

Plán údržby definuje, kdy je třeba provést úlohu předběžně plánované preventivní práce údržby na majetku. Plány údržby mohou souviset s majetkem, typy majetku, funkčními místy nebo typy funkčních míst, nejdříve však musíte vytvořit plány údržby, které mají být použity ve vaší společnosti.

Plán údržby může obsahovat více řádků plánu údržby. Typ a interval práce údržby je zadán na řádku plánu údržby. Existují dva typy řádků plánu údržby:

- Čas
- Počitadlo

Řádky plánu údržby typu „Čas“ jsou použity pro opakovanou plánovanou údržbu na základě pevného časového intervalu. Řádky rozvrhu údržby typu „Čítač“ se používají pro plánovanou nebo reaktivní údržbu na základě registrací čítačů majetku. Plán údržby může zahrnovat několik řádků plánu údržby obou typů.

>[!NOTE]
>Nejsou-li pro typ čítače majetku registrovány žádné hodnoty čítačů, budou řádky plánu údržby vynechány.

Nejprve vytvořte rozvrhy údržby, které požadujete pro preventivní práce údržby, a vyberte typy majetku, majetek, funkční místa a typy funkčních míst, které souvisí s jednotlivými plány údržby. Poté, pokud je to nutné, můžete také přidat plány údržby do majetku nebo funkčního místa, což provedete v části **Všechen majetek** \> vyberte majetek \> záložka s náhledem **Plány údržby majetku** **Všechna funkční místa** \> vyberte funkční místo \> záložka s náhledem **Plány údržby**.

Přidáte-li plán údržby k typům majetku nebo typům funkčních míst, znamená to, že při vytvoření nového majetku nebo funkčního místa s těmito typy majetku nebo typy funkčních míst bude majetek nebo funkční místo automaticky přidány do plánu údržby. Počátečním datem vztahu k plánu údržby bude aktuální datum, které může být nutné upravit.

## <a name="set-up-maintenance-plans"></a>Nastavit plány údržby

V tomto oddílu je popsáno nastavení řádků plánu údržby a příklady jejich použití.

1. Klikněte na **Správa majetku \> Nastavení \> Preventivní údržba \> Plány údržby**.

1. Zvolte **Nový** pro vytvoření nového pořadí.

1. Zadejte ID do pole **Pořadí údržby** a název do pole **Název**.

1. Do pole **Datum plánu** vložte počáteční datum, od kterého lze provést plánování v plánu údržby. Mějte na paměti, že řádky plánu údržby založené na čase mohou mít jiná data plánu.

1. Chcete-li aktivovat plán údržby, u přepínacího tlačítka **Aktivní** vyberte možnost „Ano“.

    >[!NOTE]
    >Pokud plán údržby dezaktivujete, nebudou v plánu údržby při spuštění úlohy rozvrhu údržby vytvořeny žádné příspěvky plánu.

1. Pole **Tolerance dnů před** a **Tolerance dnů po** se vztahují k řádkům rozvrhu údržby, ve kterých je zaškrtnuto políčko **Potlačit překrývající se práce údržby** (viz krok 17). Pole „Tolerance“ slouží k rozšíření intervalu ve dnech, ve kterém se během plánování rozvrhu údržby při překrytí několika rozvrhů údržby vytvoří nejkomplexnější/největší práce údržby jako řádek rozvrhu údržby, zatímco častěji se překrývající úlohy jsou při plánování rozvrhu údržby vynechány. Zadejte počet dní do pole **Tolerance dnů před**, například „2“.

1. Pokud jste do pole **Tolerance dnůpřed** vložili hodnotu, zadejte také počet dní do pole **Tolerance dnů po**, například „2“.

    >[!NOTE]
    >Příklad popsaný v tomto a předchozím kroku znamená, že pokud se překrývá několik řádků plánu údržby a pro jeden nebo více řádků je vybrána možnost **Potlačit překrývající se práce údržby**, bude období vynechání řádků rozvrhu údržby rozšířeno na celkem pět dní (očekávané počáteční datum na řádku rozvrhu údržby *a* dva dny před *a* dva dny po tomto datu).

1. V polích ve skupině **Podrobnosti** na záložce s náhledem **Podrobnosti** je zobrazen počet řádků plánu údržby nastavených v plánu údržby a počet položek majetku a funkčních míst souvisejících s plánem údržby.

1. Na záložce s náhledem **Řádky** vyberte možnost **Přidat řádek času** nebo **Přidat řádek čítače majetku** a vytvořte nový řádek plánu údržby.

1. Do pole **Popis pracovního příkazu** zadejte popis řádku. Popis je přenesen do souvisejících pracovních příkazů.

1. V poli **Typ práce údržby** vyberte typ práce, ke které se řádek plánu údržby vztahuje.

1. V polích **Varianta typu práce údržby** a **Obor** vyberte pro typ práce údržby související variantu a obor.

1. Do polí **Dokončit v řádu dnů** a **Dokončit v řádu hodin** můžete zadat očekávané koncové datum ve dnech nebo hodinách. Očekávané koncové datum je vloženo relativně k očekávanému datu zahájení, které je vypočítáno při vytvoření řádků rozvrhu údržby. Chcete-li například určit, že související úloha má být dokončena do týdne od očekávaného počátečního data, můžete do pole **Dokončit v řádu dnů** vložit hodnotu „7“.

1. V poli **Typ intervalu** vyberte typ intervalu, který má být použit na řádku plánu údržby, například „Opakovaný...“ nebo „Jednou...“. V tabulce [Přehled typů intervalů](#interval-types) níže najdete popis vztahu mezi typy intervalů a typy řádků.

1. Pole **Období** se vztahuje pouze k typům řádků založeným na čase. Vyberte typ období související s frekvencí období.

1. V poli **Frekvence období** zadejte, kolikrát má být řádek použit k plánování preventivních prací údržby. Příklad: Pokud jste vytvořili řádek typu „čítač“, čítač představuje množství výroby a do tohoto pole vložíte číslo „20 000“, během plánování preventivní údržby budou vytvořeny nové řádky pořadí údržby pokaždé, když očekáváte vyrobit 20 000 více položek.

1. Zaškrtávací políčko **Potlačit překrývající se práce údržby** se vztahuje k typům řádků založeným na čase a na čítači. Zaškrtnutím tohoto políčka odstraníte položky rozvrhu údržby, které jsou vytvořeny ke stejnému datu. To je důležité například v případě, že jste vytvořili řádek s 1měsíční kontrolou, další řádek s 6měsíční kontrolou a řádek s 1roční kontrolou. V případě 1roční kontroly chcete provést pouze tuto kontorlu, nikoli ostatní, které by se také vešly do časového rámce. Chcete-li správně replikovat tento příklad, nastavte řádek 1roční kontroly jako první řádek, řádek s 6měsíční kontrolou jako druhý řádek a řádek s 1měsíční kontrolou jako třetí řádek, a zaškrtněte políčko **Potlačit překrývající se práce údržby** na řádcích s 1- a 6měsíční kontrolou. Tímto zajistíte, že při dosažení označení 1 roku budou vynechány kontroly za jeden měsíc a šest měsíců a řádek rozvrhu údržby bude vytvořen pouze pro řádek 1roční kontroly.

    >[!NOTE]
    >Příklad popsaný v tomto kroku ukazuje, že nejúplnější úloha, která obsahuje nejvyšší počet úkolů a která se tak často neprovádí, by měla být vždy vložena jako první řádek. Častější úlohy jsou poté vloženy jako samostatné řádky v pořadí frekvence, přičemž nejčastěšjí úloha se nachází v dolní části seznamu.

1. Pole **Čítač** se vztahuje pouze k typům řádků založeným na čítači. Vyberte typ čítače, který se má použít na řádku. Není-li typ čítače aktivní v souvisejícím majetku, je řádek plánu údržby vynechán.

1. Pole **Ochranná doba čítače majetku ve dnech** se vztahuje pouze k typům řádků založeným na čítači. Zadejte číslo, které definuje, kolik dní nazpět mají být zkontrolovány registrace čítačů po provedení plánování rozvrhu údržby. To znamená, jak moc nazpět jsou data (existující registrace čítačů) použita jako základ pro výpočet trendu, který určuje, kolik řádků rozvrhu údržby bude vytvořeno.

    >*Příklad:* Pokud očekáváte, že registrace čítačů budou provedeny jednou měsíčně, můžete do tohoto pole vložit číslo „365“, protože plánování rozvrhu údržby bude vždy založeno na posledních 12 měsících, a tedy vytvářet řádky rozvrhu údržby na základě trendu minulého roku Pokud do tohoto pole zadáte číslo „10“, očekáváte, že se registrace čítačů budou provádět častěji, například denně. To znamená, že při plánování rozvrhu údržby se registrace čítačů za posledních 10 dnů použijí jako základ pro plánování řádků rozvrhu údržby.

1. Pole **Datum plánu** se vztahuje pouze k typům řádků založeným na čase. Pokud má řádek plánu údržby jiné datum plánování než celý plán údržby, vyberte datum v poli **Datum plánu** na řádku.

1. V poli **Úroveň služeb** můžete vybrat úroveň služeb pracovního příkazu jako další vymezení na řádku plánu údržby, který má být použit jako úroveň služeb v pracovních příkazech.

1. Chcete-li, aby se při vytváření plánů údržby automaticky vytvořil pracovní příkaz podle vybraného řádku plánu údržby, zaškrtněte políčko **Automaticky vytvořit**.

1. Pokud jste zaškrtli políčko **Automaticky vytvořit**, můžete v poli **Typ pracovního příkazu** vybrat typ automaticky vytvořeného pracovního příkazu. Pokud jste zaškrtli políčko **Automaticky vytvořit** a v tomto poli nevyberete typ pracovního příkazu, bude vybrán typ pracovního příkazu vybraný pod odkazem **Správa majetku \> Nastavení \> Parametry správy majetku \> Pracovní příkazy** \> **Typ preventivního pracovního příkazu**.

1. Pole **Období od** a **Období do** slouží k vytvoření opakovaného řádku plánu údržby na základě času v průběhu 12 měsíců. *Příklad:* Vybavení používané pro správu zelených oblastí vyžaduje servis každé pružiny v předdefinovaném období. Vložte počáteční datum období, které má být opakováno, do pole **Období od**.

1. Vložte koncové datum období, které má být opakováno, do pole **Období do**.

1. V poli **Výsledné období** se zobrazí aktuální období, které se má opakovat. Když aktuální období uplyne a zahájíte nový rok, bude období zobrazené v tomto poli aktualizováno tak, aby odráželo další období v posloupnosti opakování.

1. Na záložce s náhledem **Majetek** vyberte položky majetku, které mají souviset s plánem údržby.

1. Na záložce s náhledem **Typy majetku** vyberte položky majetku, které mají souviset s plánem údržby.

1. Na záložce s náhledem **Funkční místa** vyberte funkční místa, která mají souviset s plánem údržby. Pokud je to nutné, můžete upřesnit nastavení výběrem souvisejícího typu majetku, výrobce a modelu.

1. Na záložce s náhledem **Typy funkčních míst** vyberte typy funkčních míst, které mají souviset s plánem údržby.

>[!NOTE]
>Pokud jsou pro majetek, na který se vztahuje záruka dodavatele, vytvořeny pracovní příkazy ručně, zobrazí se dialogové okno, které uživatele upozorní na záruku. Vytvoření pracovního příkazu lze v tuto chvíli zrušit. Kontrola vztahu záruky je vynechána pro automaticky vytvořené pracovní příkazy.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Přehled typů intervalů

| Typ a popis intervalu | Typ řádku: čas | Typ řádku: čítač |
|---|---|---|
| **Typ intervalu: opakováno od data plánu** Počet začíná datem, které bylo použito. Při vytváření plánů údržby se po dosažení intervalu vytvoří řádky rozvrhu údržby. | Použije se **Datum plánu** na řádku plánu údržby. Pokud není na řádku vybráno žádné datum plánu, použije se **Datum plánu** pro plán údržby. Příklad: Pokud je v poli **Frekvence období** vloženo číslo „3“ a v poli **Období** je vybrána hodnota „rok“, bude nový řádek plánu údržby vytvořen každé 3 roky. | Použije se **Datum plánu** pro řádek plánu údržby. Pokud byl čítač nahrazen, použije se jako datum plánu poslední datum nahrazení. |
| **Typ intervalu: Opakováno od počátečního data** Počet začíná od počátečního data vztahu majetku. Datum je vybráno v zobrazení podrobností **Všechen majetek** na záložce s náhledem \> **Plány údržby majetku** pole \> **Počáteční datum** nebo v zobrazení podrobností **Všechna funkční místa** záložka s náhledem \> **Plány údržby** pole \> **Počáteční datum**. Při vytváření plánů údržby se po dosažení intervalu vytvoří řádek rozvrhu údržby. | Pro majetek nebo funkční místo se použije počáteční datum řádku plánu údržby. Je-li toto pole prázdné, použije se **Datum plánu** pro plán údržby. | Pro majetek nebo funkční místo se použije počáteční datum řádku plánu údržby. Je-li toto pole prázdné, použije se **Datum plánu** pro plán údržby. |
| **Typ intervalu: Opakováno od posledního pracovního příkazu** Počet začíná skutečným koncovým datem a časem posledního pracovního příkazu, který byl dokončen na majetku s tímto konkrétním typem úlohy údržby a kombinaci varianty typu práce údržby a oboru. Toto datum a čas jsou zobrazeny v poli **Skutečné dokončení** v zobrazení podrobností **Všechny pracovní příkazy**. | Skutečné datum a čas ukončení pracovního příkazu dokončeného na majetku s tímto konkrétním typem práce údržby / varianty typu práce údržby / oboru. Pokud nebyl nalezen žádný dokončený pracovní příkaz, použije se místo toho jedno z dat použitých v typu interval "Opakováno od počátečního data". | Skutečné datum a čas ukončení pracovního příkazu dokončeného na majetku *a* kombinaci typu práce údržby / varianty typu práce údržby / oboru. se používá. Pokud nebylo do pracovního příkazu zadáno koncové datum a čas, použije se místo toho jedno z dat použitých v typu interval "Opakováno od počátečního data". |
| **Typ intervalu: Jednou od data plánu**, viz popis pro typ intervalu „Opakováno od data plánu“ uvedený výše. Jediný rozdíl je, že tento typ intervalu lze použít pouze jednou. | Další informace naleznete v popisu intervalu typu „Opakováno od data plánu“ výše. Tento interval se obvykle používá pro jednorázovou údržbu nebo servisní práci. | Další informace naleznete v popisu intervalu typu „Opakováno od data plánu“ výše. Tento interval se obvykle používá pro jednorázovou údržbu nebo servisní práci. **Poznámka 1:** Tento typ intervalu je vhodný pouze v případě, že je čítač nahrazen při každém provedení údržby nebo servisní práce. Pokud byl z nějakého důvodu čítač nahrazen před koncem plánovaného intervalu, bude pro úlohu vypočten nový čas od okamžiku nahrazení čítače. **Poznámka 2:** Pokud je čítač při dokončení údržby nebo servisní práce nahrazen, bude tento typ intervalu fungovat jako výše uvedený typ "Opakováno od data plánu". |
| **Typ intervalu: Jednou od počátečního data**, viz popis pro typ intervalu „opakováno od počátečního data“ uvedený výše. Jediný rozdíl je, že tento typ intervalu lze použít pouze jednou. | Další informace naleznete v popisu intervalu typu „Opakováno od počátečního data“ výše. Tento interval se obvykle používá pro jednorázovou údržbu nebo servisní práci. | Další informace naleznete v popisu intervalu typu „Opakováno od počátečního data“ výše. Tento interval se obvykle používá pro jednorázovou údržbu nebo servisní práci. **Poznámka 1** výše je použita také pro tento typ intervalu. **Poznámka 3:** Pokud je čítač při dokončení údržby nebo servisní práce nahrazen, bude tento typ intervalu fungovat jako výše uvedený typ „Opakováno od počátečního data“. |
| **Typ intervalu: Po dosažení horní hodnoty** Tento typ intervalu platí pouze čítače a používá se k označení horního limitu nastaveného v řádku plánu údržby. Položky rozvrhu údržby budou mít očekávané počáteční datum a čas registrace čítače, což znamená, že tyto položky budou vytvořeny s očekávaným počátečním datem, které se rovná nebo předchází systémovému datu. | Nelze použít | Interval počítadla označuje horní limit. Je-li tento limit překročen při vytváření registrace čítače, vytvoří se řádek rozvrhu údržby při plánování preventivní údržby. |
| **Typ intervalu: Po dosažení spodní hodnoty** Tento typ intervalu platí pouze čítače a používá se k označení dolního limitu nastaveného v řádku plánu údržby. Položky rozvrhu údržby budou mít očekávané počáteční datum a čas registrace čítače, což znamená, že tyto položky budou vytvořeny s očekávaným počátečním datem, které se rovná nebo předchází systémovému datu. | Nelze použít | Interval počítadla označuje dolní limit. Je-li tento limit překročen při vytváření registrace čítače, vytvoří se řádek rozvrhu údržby při plánování preventivní údržby. |
| **Typ intervalu: propojeno od počátečního data** tento typ intervalu vytváří pouze řádek plánu údržby. Plán údržby může obsahovat více řádků plánu s použitím tohoto typu intervalu a tyto řádky budou propojeny. Obvykle vytvoříte plán údržby, který obsahuje řádky pouze tohoto typu intervalu. Řádky rozvrhu údržby jsou vytvořeny pomocí rozpoznání řádku plánu údržby, který má první očekávané počáteční datum a čas. | Další informace naleznete v popisu intervalu typu „Jednou od počátečního“ výše. Příklad: Vytvoříte dva řádky plánu údržby pro servisní práci na automobilu: jeden řádek založený na čase s 1letým obdobím a jeden řádek založený na čítači s limitem 25 000 km. Řádek rozvrhu údržby se vytvoří pro limit, který je dosažen jako první. Pro tento typ řádku vytvoříte řádek s 1letým obdobím. | Další informace naleznete v popisu intervalu typu „Jednou od počátečního“ výše. Příklad: Vytvoříte dva řádky plánu údržby pro servisní práci na automobilu: jeden řádek založený na čase s 1letým obdobím a jeden řádek založený na čítači s limitem 25 000 km. Řádek rozvrhu údržby se vytvoří pro limit, který je dosažen jako první. Pro tento typ řádku vytvoříte řádek s limitem 25 000 km. Příklad vytvoření dvou řádků čítače: Můžete také vytvořit rozvrh údržby se dvěma propojenými řádky založenými na čítačích, ve kterých má první řádek limit 10 000 položek a druhý řádek se vztahuje k strojnímu nebo pracovnímu centru vyžadujícímu servis po 3 000 hodinovém provozu. |
| **Typ intervalu: propojeno od posledního pracovního příkazu** Tento typ intervalu vytváří nové řádky plánu údržby po každém dokončeném řádku pracovního příkazu. Plán údržby může obsahovat více řádků plánu s použitím tohoto typu intervalu a tyto řádky budou propojeny. Obvykle vytvoříte plán údržby, který obsahuje řádky plánu údržbu pouze tohoto typu intervalu. Řádky rozvrhu údržby jsou vytvořeny pomocí rozpoznání řádku plánu údržby, který má první očekávané počáteční datum a čas. | Tento typ intervalu funguje v podstatě stejně jako typ "Propojeno od počátečního data" popsaný výše. Jediný rozdíl je v datu, na kterém je typ intervalu založen. Použité datum je skutečné datum a čas posledního pracovního příkazu dokončeného na majetku *a* kombinaci typu práce údržby / varianty typu práce údržby / oboru. | Tento typ intervalu funguje v podstatě stejně jako typ "Propojeno od počátečního data" popsaný výše. Jediný rozdíl je v datu, na kterém je typ intervalu založen. Použité datum je skutečné datum a čas posledního pracovního příkazu dokončeného na majetku *a* kombinaci typu práce údržby / varianty typu práce údržby / oboru. |
| **Typ intervalu: Opakovaný na agregované hodnotě (pouze počítadlo)** Když je spuštěn plán údržby, bude naplánovaný řádek plánované údržby vytvořen pokaždé, když akumulovaná hodnota pro počitadlo majetku dosáhne frekvence období nebo dokonce násobku frekvence období. (Četnost období je definováno na řádku plánu údržby.)<p>Další informace o tom, jak tuto funkci povolit a používat, najdete v části [Vylepšení údržby založené na počítadle](#counter-based-maintenance) dále v tomto tématu. | Nelze použít | **Příklad:** Počítadlo hodin je nastaveno pro majetek AK-101. Pro majetek je také nastaven řádek plánu majetku. Typ intervalu tohoto řádku je *Opakováno na agregovanou hodnotu (pouze počítadlo)* a periodická frekvence je *1000*. Když je spuštěn plán údržby, vygeneruje se řádek plánované údržby, když agregovaná hodnota čítače přesáhne 1 000 hodin. Poté, když agregovaná hodnota čítače přesáhne 2 000 hodin, bude vygenerován další řádek plánované údržby atd. každých dalších 1 000 hodin. |
| **Typ intervalu: Jakmile je na agregované hodnotě (pouze počítadlo)** Když je spuštěn plán údržby, bude naplánovaný řádek plánované údržby vytvořen pokaždé, když akumulovaná hodnota čítače dosáhne frekvence období, která je definována na řádku plánu údržby.<p>Další informace o tom, jak tuto funkci povolit a používat, najdete v části [Vylepšení údržby založené na počítadle](#counter-based-maintenance). | Nelze použít | **Příklad:** Počítadlo hodin je nastaveno pro majetek AK-101. Pro majetek je také nastaven řádek plánu majetku. Typ intervalu tohoto řádku je *Jednou na agregovanou hodnotu (pouze počítadlo)* a periodická frekvence je *1000*. Když je spuštěn plán údržby, vygeneruje se řádek plánované údržby, když agregovaná hodnota čítače přesáhne 1 000 hodin. |

>[!NOTE]
>Když jsou řádky plánu údržby na bázi času vytvořeny řádky rozvrhu údržby, očekávaný čas je vždy na začátku dne. V případě řádků plánu údržby na bázi čítačů může být očekávaný čas kdykoli v průběhu dne.

Níže se nachází příklady nastavení řádků plánu údržby s časovým rozlišením a na základě čítačů:

**Příklad 1 – Řádek plánu údržby na základě času:** Úloha namazání může být nastavena v pevném intervalu a dojde k ní jednou týdně. Pro tento účel vyberte v poli **Typ intervalu** hodnotu „Opakováno od data plánu“. Viz příklad na následujícím obrázku.

![Servisní úloha nastavená v pevném intervalu, vyskytující se jednou týdně](media/02-preventive-maintenance.png "Servisní úloha nastavená v pevném intervalu, vyskytující se jednou týdně")

**Příklad 2 – Řádek práce údržby na základě času:** Úlohu kontroly lze nastavit tak, aby byla provedena přibližně jednou týdně. Pro tento účel vyberte v poli **Typ intervalu** hodnotu „Opakováno od posledního pracovního příkazu“. Viz příklad na následujícím obrázku.

![Přibližně jednou týdně je nastavena úloha kontroly](media/03-preventive-maintenance.png "Přibližně jednou týdně je nastavena úloha kontroly")

**Příklad: 3 – Řádek plánu údržby na základě čítače:** Následující grafické znázornění ukazuje hodinové počitadlo, pro které je vytvořen nový řádek plánu údržby při každém 250 hodin. Typ intervalu pro tento řádek založený na čítači je opakován od počátečního data. Počáteční datum představuje počáteční datum souvisejících položek majetku v zobrazení podrobností **Všechen majetek** \> záložka s náhledem **Plány údržby majetku** \> pole **Počáteční datum** nebo v zobrazení podrobností **Funkční místo** \> záložka s náhledem **Plány údržby** pole \> **Počáteční datum**. Toto je příklad plánu *preventivní* údržby, protože řádek rozvrhu údržby je automaticky vytvořen pokaždé, když je dosaženo prahové hodnoty (+250).

![Čítač hodin, který pravidelně vytváří řádky plánu údržby](media/04-preventive-maintenance.png "Čítač hodin, který pravidelně vytváří řádky plánu údržby")

**Příklad 4 – Řádek plánu údržby založený na čítači** : Následující grafické znázornění ukazuje snížení hodnoty čítače s měřením opotřebení brzdových destiček. Řádek rozvrhu údržby se vytvoří, když je na brzdové destičce vytvořena registrace čítače pod 20 mm. Typ intervalu pro tento řádek založený na čítači je „Po dosažení spodní hodnoty“ nebo „Od posledního počátečního data“. Toto je příklad plánu *reaktivní* údržby, protože řádek rozvrhu údržby není vytvořen až do doby, než je registrováno měření pod 20 mm.

![Snížení hodnoty čítače, měření opotřebení brzdových destiček](media/05-preventive-maintenance.png "Snížení hodnoty čítače, měření opotřebení brzdových destiček")

**Příklad 5 – Řádek plánu údržby založený na čítači:** Následující grafické znázornění ukazuje čítač s prahovou hodnotou -18°C. Řádek rozvrhu údržby se vytvoří po provedení registrace čítače nad -18°C. Typ intervalu pro tento řádek založený na čítači je „Po dosažení horní hodnoty“. Toto je příklad plánu *reaktivní* údržby, protože řádek rozvrhu údržby není vytvořen až do doby, než je registrováno měření vyšší než -18°C.

![Počítadlo s prahovou hodnotou -18 °C](media/06-preventive-maintenance.png "Počítadlo s prahovou hodnotou -18 °C")

- Když vytvoříte nový majetek a tento majetek používá typ související s plánem údržby, plán údržby se automaticky vloží do umístění **Všechny objekty \> záložka s náhledem Plány údržby majetku**. V části **Výchozí nastavenítypu majetku** na záložce s náhledem **Plány údržby** budou automaticky vloženy související plány údržby.
- Pokud přidáte nebo odeberete typy majetku nebo funkčních míst v **plánech údržby**, tato změna se projeví pouze u nových položek majetku vytvořených po provedení změny.
- Pokud přidáte nebo odeberete majetek nebo funkční místa v **Plánech údržby**, tato změna se automaticky aktualizuje v umístění **Všechen majetek záložky s náhledem \> Plány údržby majetku** nebo **Všechna funkční místa \> záložka s náhledem Plány údržby**.

Na následujícím obrázku je znázorněn příklad plánu údržby "nákladní vozík" na stránce **Plány údržby**.

![Příklad plánu údržby nákladních vozidel](media/07-preventive-maintenance.png "Příklad plánu údržby nákladních vozidel")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Přidání plánu údržby do majetku

1. Jděte na **Správa majetku \> Společné \> Majetek \> Všechen majetek** nebo **Aktivní majetek**.

1. Vyberte majetek, pro který chcete nastavit plán údržby, a vyberte tlačítko **Upravit**.

1. Na pevné záložce **Plány údržby majetku** klinutím na **Přidat řádek** přidejte plán údržby do majetku.

1. V poli **Plán údržby** vyberte relevantní plán údržby.

1. V poli **Počáteční datum** vyberte počáteční datum, od kterého lze provést plánování preventivních prací údržby. 

1. Zvolte **Uložit**. Pole **Aktivní** je aktualizováno automaticky.

Na následujícím obrázku je znázorněn příklad plánů údržby nastavených u majetku na stránce **Všechny majetky**.

![Příklad plánů údržby nastavených na majetku](media/08-preventive-maintenance.png "Příklad plánů údržby nastavených na majetku")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Vylepšení údržby založené na počítadle

Funkce *Vylepšení údržby založené na počítadle* zavádí následující funkce:

- Možnost automaticky vložit čítač, který má hodnotu *0* (nula) při vytvoření majetku. Tato možnost může být užitečná, když používáte prediktivní údržbu založenou na počítačích. Když se funkce *Vylepšení údržby založené na čítači* nepoužívá, čítače, které mají hodnotu *0* (nula), musí být vloženy ručně.
- Možnost nakonfigurovat čítač tak, aby se automaticky resetoval po dokončení pracovního příkazu. Tato funkce je užitečná, pokud chcete naplánovat údržbu na základě agregované hodnoty od dokončení posledního pracovního příkazu.
- Je pojmenován nový typ intervalu plánu údržby *Opakováno na agregovanou hodnotu (pouze čítač)*. Tento typ spouští údržbu pokaždé, když agregovaný čítač dosáhne násobku konkrétní hodnoty. Například údržbu lze spustit každých 10 000 hodin. Více informací naleznete v části [Přehled typů intervalu](#interval-types) výše v tomto tématu.
- Je pojmenován další nový typ intervalu plánu údržby *Jednou na agregovanou hodnotu (pouze čítač)*. Tento typ spouští údržbu pokaždé, když agregovaný čítač dosáhne násobku konkrétní hodnoty, například 8 000 hodin. Více informací naleznete v části [Přehled typů intervalu](#interval-types).

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Zapnutí funkce vylepšení údržby založené na čítači

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Správa majetku*
- **Název funkce:** *Vylepšení údržby založené na čítači*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Vytvoření a inicializace čítačů, když je vytvořen majetek

Pokaždé, když vytvoříte majetek, související čítače majetku, které se inicializují na hodnotu *0* (nula), lze automaticky vytvořit za předpokladu, že nastavíte systém a majetek vytvoříte správně.

1. Přejděte na **Správa majetku \> Nastavení \> Typy majetku**.
1. Ujistěte se, že máte typ majetku, který je použitelný pro váš plánovaný nový majetek. Podle potřeby vytvořte typ majetku. Ujistěte se, že jsou všechny vybrané čítače vybrány na záložce s náhledem **Čítače**.
1. Přejděte na **Správa majetku \> Nastavení \> Typy majetku \> Čítače**.
1. U každého příslušného počítadla se ujistěte, že je pole **Celkový souhrn** nastaveno na *Součet*.
1. Na stránce **Všechen majetek** vytvořte majetek.
1. Nastavte pole **Typ majetku** na typ majetku, který jste identifikovali nebo vytvořili v kroku 2.
1. Dokončete nastavení nového majetku podle potřeby.
1. Přejděte na **Správa majetku \> Dotazy \> Majetek \> Čítače**. Měli byste být schopni najít inicializované čítače, které jsou nastaveny pro váš nový majetek.

> [!NOTE]
> Když se vytvoří inicializované čítače majetku, předpokládá se, že majetek nebyl před přidání do systému nikdy použit. Když je plán údržby spuštěn poprvé, výpočet používá datum a hodnotu čítače *0* (nula) jako základ pro výpočet budoucí údržby. Pokud majetek nebyl nový, když byl přidán do systému, můžete ručně upravit hodnotu čítače tak, aby odpovídala skutečné hodnotě čítače. Chcete-li upravit hodnotu čítače, otevřete příslušný majetek na stránce **Všechen majetek** a pak v podokně akcí na kartě **Majetek** ve skupině **Preventivní** vyberte **Čítače**. Na stránce **Čítače majetku** pro vybraný majetek upravte hodnotu ve sloupci **Hodnota** pro počáteční záznam počitadla podle potřeby.

### <a name="automatically-reset-a-counter-value"></a>Automaticky vynulovat hodnotu čítače

Můžete nakonfigurovat systém tak, aby automaticky vynuloval čítač pokaždé, když příslušný pracovní příkaz dosáhne vybrané hodnoty stavu.

1. Klikněte na **Správa majetku \> Nastavení \> Preventivní údržba \> Plány údržby**.
1. V podokně seznamu vyberte plán údržby. Resetování čítače se použije na všechen majetek, který používá tento plán.
1. V sekci **Řádky** najděte řádek čítače aktiv, pro který chcete vynulovat čítač, a zaškrtněte políčko **Vynulovat čítač** pro daný řádek. (Řádky čítače majetku mají hodnotu ve sloupci **Čítač**. Čítač, který je uveden v tomto sloupci, je čítač, který bude vynulován pro příslušný majetek.)
1. Jděte na **Správa majetku \> Nastavení \> Pracovní příkazy \> Stavy životního cyklu**.
1. V podokně seznamu vyberte stav životního cyklu pracovního příkazu, na kterém by měl být vynulován příslušný čítač.
1. Na pevné záložce **Obecné** nastavte možnost **Resetovat čítač** na *Ano*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]