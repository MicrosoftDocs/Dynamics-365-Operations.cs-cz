---
title: Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby
description: Tohle téma popisuje kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby ve Správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9efbd9651f6a2fa57e761238c6acfe6111e986e6
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874755"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Typ majetku je připojen ke každému majetku. Typy majetku definují typy práce údržby (a tudíž i práce údržby), které lze provést na majetku. Při vytvoření pracovního příkazu musíte vybrat typ práce údržby. Můžete vybrat pouze typy prací údržby, které souvisí s nastavením typu majetku použitém pro daný majetek.

Grafický přehled položek majetku a typů prací údržby a jejich propojení s pracovními příkazy naleznete v tématu [Majetek a pracovní příkazy](../overview/functional-locations-and-objects.md).

Pro typ práce údržby lze nastavit varianty typu práce údržby. Varianty typu práce údržby definují varianty typu práce, například z hlediska velikosti (malá, střední nebo velká), období (týdně, obtýden, měsíčně nebo každé tři měsíce) a konfigurace (nízký standard, pružná nebo vysoký výkon).

Obory práce údržby poskytují informace o profesionálních trzích týkající se obchodování například s mechanickými, elektrickými nebo hydraulickým zbožím. Pro obor práce údržby mohou být nastaveny požadavky na kompetenci. Všechny obory práce údržby lze použít ve vztahu ke všem typům práce údržby. Výběr varianty typu práce údržby a/nebo oboru práce údržby na pracovním příkazu je nepovinný.

Pro každý typ práce údržby lze vytvořit varianty nastavení typu práce údržby. Máte-li například typ práce údržby s názvem **Služba**, můžete pro tuto práci údržby vytvořit následující varianty: **Nákladní automobily 30 000 km**, **Automobily 30 000 km** a **Dodávky 30 000 km**.

Kategorie typů práce údržby se používají ke shromažďování skupin typů práce údržby pro účely přehledu. Kategorie typů práce údržby mohou být například tyto: **Kalibrace**, **Kontrola**, **Generální oprava** a **Instrumentace**.

Šablony a proměnné kontrolních seznamů údržby se používají k nastavení kontrolních seznamů údržby. Kontrolní seznamy údržby se nastavují pro typy práce údržby a používají se v pracovních příkazech.

Nejprve nastavíte požadované kategorie typů práce údržby, varianty typů práce údržby a obory práce údržby. Poté vytvoříte typy práce údržby. Nakonec na stránce **Výchozí nastavení typu práce údržby** vytvoříte všechny varianty typů práce údržby, které jsou požadovány pro vaše zařízení. Na této stránce můžete také nastavit prognózy, kontrolní seznamy údržby a nástroje pro kombinaci typů práce údržby.

> [!NOTE]
> Typ práce údržby může souviset s pouze jednou kategorií typu práce údržby.

## <a name="create-a-maintenance-job-type-category"></a>Vytvoření kategorie typu práce údržby

1. Vyberte **Správa majetku** \> **Nastavení** \> **Práce** \> **Kategorie typu práce údržby**.
2. Zvolte **Nové**.
3. V poli **Kategorie typu práce údržby** zadejte ID pro kategorii typu práce údržby.
4. Do pole **Název** zadejte název.

    Po přidružení kategorií typů práce údržby k typům práce údržby se v poli **Typy práce** zobrazí počet typů práce údržby, které se vztahují k této kategorii typů práce údržby.

![Obrázek č. 1](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Vytvoření varianty typu práce údržby

1. Vyberte **Správa majetku** \> **Nastavení** \> **Práce** \> **Varianty typu práce údržby**.
2. Zvolte **Nové**.
3. V poli **Varianta typu práce údržby** zadejte ID pro variantu typu práce údržby.
4. Zadejte popis do pole **Popis**.
5. Na záložce s náhledem **Typy práce údržby** přidejte typ práce údržby možností **Přidat**.
6. V poli **Typ práce údržby** vyberte typ práce údržby.
7. Opakováním kroků 5 až 6 přidejte do varianty typu práce údržby další typy práce údržby.

    Na záložce s náhledem **Podrobnosti** zobrazuje pole **Typy práce** počet typů prací údržby, které byly přidány do této varianty typu práce údržby.

![Obrázek č. 2](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Vytvoření oboru práce údržby

1. Vyberte **Správa majetku** \> **Nastavení** \> **Práce** \> **Obor práce údržby**.
2. Zvolte **Nové**.
3. V poli **Obor** zadejte ID oboru práce údržby.
4. Zadejte popis do pole **Popis**.
5. Na záložce s náhledem **Dovednosti** pomocí možnosti **Přidat** přidáte novou dovednost, která by měla souviset s oborem práce údržby.
6. V poli **Dovednost** vyberte dovednost.
7. V poli **Úroveň** vyberte úroveň dovednosti.
8. Zopakováním kroků 5 až 7 přidáte další dovednosti do oboru práce údržby.

    Na záložce s náhledem **Podrobnosti** zobrazuje pole **Dovednosti** počet dovedností, které byly přidány do tohoto oboru práce údržby.

9. Na záložce s náhledem **Certifikáty** pomocí možnosti **Přidat** přidejte certifikát do oboru práce údržby.
10. V poli **Typ certifikátu** vyberte certifikát.
11. Zopakováním kroků 9 až 10 přidáte další certifikáty do oboru práce údržby.

    Na záložce s náhledem **Podrobnosti** zobrazuje pole **Certifikáty** počet certifikátů, které byly přidány do tohoto oboru práce údržby.

![Obrázek č. 3](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Vytvoření proměnné kontrolního seznamu údržby

Když vytváříte řádky kontrolního seznamu údržby ve výchozím nastavení typu práce údržby, je nutné vybrat typ kontrolního seznamu údržby. **Proměnná** je jedním z typů kontrolního seznamu údržby. Používá se k definování možného výsledku v rozsahu na řádku kontrolního seznamu údržby, který souvisí s řádkem pracovního příkazu. Proměnná umožňuje vytvořit sadu předdefinovaných výsledků, aniž by bylo nutné provést přesné měření.

**Příklad 1:** Úroveň oleje můžete měřit definováním tří hodnot: **Úroveň je příliš vysoká**, **Úroveň je příliš nízká** a **Úroveň je v rozsahu**. Pro každou hodnotu definujete, zda je výsledná hodnota **Úspěch**, **Neúspěch** nebo **Nic**.

**Příklad 2:** Prohlédnete si některé zařízení s cílem ohodnotit jeho opotřebení.

1. Vyberete **Správa majetku** \> **Nastavení** \> **Kontrolní seznamy údržby** \> **Proměnné kontrolních seznamů údržby**.
2. Zvolte **Nové**.
3. V poli **Proměnná** zadáte ID proměnné kontrolního seznamu údržby.
4. Do pole **Název** zadejte název.
5. Na záložce s náhledem **Obecné** výběrem možnosti **Přidat** přidáte řádek pro proměnnou.

    Do pole **Číslo řádku** se automaticky zadá pořadové číslo řádku. Po přidání všech řádků můžete čísla řádků podle potřeby změnit. Když vyberete řádek a potom stisknete klávesu **se šipkou dolů**, další číslo v posloupnosti se automaticky zapíše do dalšího řádku.

6. V poli **Hodnota** zadejte popis hodnoty.
7. V poli **Výsledek** vyberte pro řádek výsledek.

![Obrázek č. 4](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Vytvoření šablony kontrolního seznamu údržby

Šablony kontrolního seznamu údržby lze použít jako běžnou sadu úkolů, které musí pracovník provést, aby mohl správně dokončit pracovní příkaz. Na šablony je odkazováno z řádků kontrolního seznamu údržby výchozího typu práce údržby. Na šablony lze odkazovat přes více výchozích řádků typu práce údržby. Lze tedy snadno opakovaně používat sadu běžných úkolů kontrolního seznamu údržby. Příklady šablon kontrolního seznamu údržby zahrnují obecné bezpečnostní pokyny a seznam položek a podmínek, které musí být zkontrolovány na určitém čerpadlu nebo podobných modelech pásu dopravníku.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Kontrolní seznamy údržby** \> **Šablony kontrolních seznamů údržby**.
2. Zvolte **Nové**.

    ID šablony je automaticky zadáno do pole **Šablona kontrolního seznamu údržby**.

3. Do pole **Název** zadejte název šablony kontrolního seznamu údržby.
4. Na záložce s náhledem **Řádky kontrolního seznamu údržby** možností **Přidat** přidejte řádek šablony.

    Do pole **Číslo řádku** se automaticky zadá pořadové číslo řádku. Po přidání všech řádků můžete čísla řádků podle potřeby změnit. Když vyberete řádek a potom stisknete klávesu **se šipkou dolů**, další číslo v posloupnosti se automaticky zapíše do dalšího řádku.

5. V poli **Typ** vyberte typ řádku kontrolního seznamu údržby. Na záložce s náhledem **Podrobnosti řádku** jsou pro každý typ kontrolního seznamu údržby zobrazeny související pole. K dispozici jsou následující hodnoty:

    - **Text** – řádek obsahuje text, který popisuje, co dělat. Tento typ kontrolního seznamu údržby použijte v případě, že chcete, aby pracovník mohl zkontrolovat nebo prohlédnout nějaký objekt, ale neočekáváte určitý (měřitelný) výsledek. Po výběru tohoto typu zadejte do pole **Název** jeho název nebo nadpis. V poli **Pokyny** zadejte popis toho, co má být provedeno. Je-li krok povinný pro kontrolní seznam údržby, volbu **Povinné** nastavte na hodnotu **Ano**.
    - **Záhlaví** – řádek se používá jako záhlaví kvůli seskupení řádků kontrolního seznamu údržby, který se zobrazí pod ním. Tento typ je užitečný v případě, že máte několik řádků kontrolního seznamu údržby, které lze rozdělit na určité oblasti. Záhlaví poskytují přehled pracovníkovi, který provede kontrolní seznam údržby s mnoha řádky. Po výběru tohoto typu zadejte do pole **Název** jeho popisný název.
    - **Šablona** – řádek slouží k vytvoření odkazu na existující šablonu. Po výběru tohoto typu zadejte do pole **Název** název šablony. V poli **Šablona** vyberte šablonu.
    - **Proměnná** – řádek slouží k definování možného výsledku v rozsahu. Informace o nastavení proměnných kontrolního seznamu údržby naleznete v oddílu [Vytvoření proměnné kontrolního seznamu údržby](#create-a-maintenance-checklist-variable). Po výběru tohoto typu zadejte do pole **Název** popisný název proměnné. V poli **Proměnná** zvolte proměnnou. V poli **Pokyny** zadejte popis toho, co má být provedeno. Je-li krok povinný pro kontrolní seznam údržby, volbu **Povinné** nastavte na hodnotu **Ano**.
    - **Měření** – řádek slouží k zaznamenání určitého měření. Můžete nastavit měření, které se má vztahovat k předdefinovanému čítači. Po výběru tohoto typu zadejte do pole **Název** název šablony. Je-li tento krok povinný pro kontrolní seznam údržby, volbu **Povinné** nastavte na hodnotu **Ano**. Chcete-li použít řádek měření jako registraci čítače, vyberte čítač v poli **Čítač**. Související pole **Jednotka** je poté automaticky aktualizováno. Pokud jste vybrali čítač, v poli **Hodnota** vyberte metodu aktualizace. V poli **Min. hodnota** a **Max. hodnota** zadejte povolený rozsah hodnot. V poli **Pokyny** zadejte popis toho, co má být provedeno.

        > [!NOTE]
        > Jakýkoli řádek typu **Měření**, pro který není nastaven čítač, je považován za nezávislou registraci měření, kde není k dispozici automatické zpracování v modulu Správa majetku. Podobně, pokud není u majetku souvisejícího s pracovním příkazem dostupný vybraný typ čítače, úkol kontrolního seznamu údržby bude považován za nezávislé měření. Hodnotu čítače lze víckrát změnit. Není zaúčtována, dokud se nezmění [stav životního cyklu pracovního příkazu](work-order-lifecycle-states.md) na stav, kde je možnost **Kontrolní seznam údržby procesu** nastaven na hodnotu **Ano**.

    Na záložce s náhledem **Podrobnosti** zobrazuje pole **Kontroly** celkový počet řádků kontrolního seznamu ve vaší šabloně. Toto číslo zahrnuje vnořené řádky v jakékoli existující šabloně, na kterou jste odkazovali ve své šabloně.

![Obrázek č. 5](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Vytvoření typu práce údržby

1. Vyberte **Správa majetku** \> **Nastavení** \> **Práce** \> **Typy práce údržby**.
2. Zvolte **Nové**.
3. V poli **Typ práce údržby** zadejte ID pro typ práce údržby.
4. Do pole **Název** zadejte název.

    Na záložce s náhledem **Podrobnosti** je zobrazen přehled počtu variant typů práce údržby, dovedností, certifikátů, následných prací a typů majetku, které byly vytvořeny pro tento typ práce údržby. V poli **Řádky nastavení** se zobrazuje počet výchozích řádků typu práce údržby, které byly nastaveny pro tuto práci údržby. Pole **Majetek** zobrazuje počet aktivních položek majetku, které aktuálně používají tento typ práce údržby.

5. Na záložce s náhledem **Obecné** v poli **Kategorie typu práce údržby** vyberte kategorii typu práce údržby.
6. Pokud typ práce údržby vyžaduje zastavení údržby zařízení před provedením práce, nastavte možnost **Aktivity prostojů údržby** na hodnotu **Ano**.
7. Na záložce s náhledem **Popis** zadejte popis typu práce údržby.
8. Na záložce s náhledem **Varianty typu práce údržby** můžete přidat varianty typy práce údržby.
9. Na záložkách s náhledem **Požadované dovednosti** a **Požadované certifikáty** můžete do typu práce údržby přidat dovednosti a požadavky na certifikáty.
10. Je-li nutné následně provést konkrétní typ práce údržby, přidejte jej na záložku s náhledem **Následující práce**. Můžete také nastavit variantu typu práce údržby a obor, které souvisejí s typem práce údržby. Pokud by následující práce měla začít určitý počet dní před nebo po zahájení práce, která používá tento typ práce údržby, zadejte počet dní do pole **Zpoždění podle dnů.** Kladná čísla představují dny po zahájení související práce a záporná čísla představují dny před naplánovaným zahájením související práce. Zadáte -li například hodnotu **5**, bude následná práce začínat pět dní po zahájení práce, která souvisí s typem práce údržby. Zadáte -li hodnotu **-3**, bude následná práce začínat tři dny před plánovaným zahájením práce, která souvisí s typem práce údržby.

    > [!NOTE]
    > Pokud přidáte více než jeden řádek typu práce údržby, posloupnost řádků označuje pořadí, ve kterém se mají provádět. Posloupnost začíná na začátku seznamu.

11. Na záložce s náhledem **Typy majetku** můžete k typu práce údržby přidat typy majetku.

![Obrázek č. 6](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Vytvoření výchozích řádků typu práce údržby a související prognózy, kontrolní seznamy údržby, nástroje, popis a přílohy

1. Vyberte **Správa majetku** \> **Nastavení** \> **Práce** \> **Výchozí natavení typu práce údržby**.

    - nebo -

    Vyberte **Typ majetku** \> **Nastavení** \> **Práce** \> **Typy práce údržby**, vyberte typ práce údržby a poté vyberte **Výchozí nastavení typu práce údržby**.

2. Zvolte **Nové**.
3. V polích **Funkční místo**, **Typ majetku**, **Výrobce**, **Model** a **Majetek** vyberte příslušné hodnoty v závislosti na tom, jak konkrétní má být výchozí typ práce údržby.
4. V poli **Typ práce údržby** vyberte typ práce údržby, pokud není automaticky vybrán.
5. V polích **Varianta typu práce údržby** a **Obor** vyberte podle potřeby variantu typu práce údržby a obor práce údržby.
6. Vyberte možnost **Prognóza**.
7. Na stránce **Výchozí prognóza typu práce údržby** můžete vytvářet prognózy pro hodiny, položky a výdaje. Na příslušných kartách vyberte možnost **Přidat** a proveďte výběr pro vytvoření požadovaných prognóz pro typ práce údržby.
8. Na kartě **Prognóza položky** můžete vybrat dimenze zásob, které mají být zobrazeny na řádku položky. Vyberte **Zásoby** \> **Dimenze**, vyberte dimenze, které chcete zobrazit, nastavte možnost **Uložit nastavení** na hodnotu **Ano** a poté vyberte tlačítko **OK**.
9. Na kartě **Prognóza položky** výběrem možnosti **Kde byla položka použita** zobrazíte přehled o tom, kde se ve Správě majetku používá položka na vybraném řádku ve vztahu k majetku, výchozímu typu práce údržby, náhradním dílům a pracovním příkazům. 

    Na záložce s náhledem **Součty prognóz údržby** se zobrazuje přehled celkových prognóz. Tento přehled zahrnuje celkový počet hodin a řádky prognózy, které byly vytvořeny.

    > [!NOTE]
    > Chcete-li zkopírovat nastavení prognózy z jiného typu práce údržby, vyberte možnost **Kopírovat prognózu** a poté vyberte typ práce údržby, ze kterého se má nastavení zkopírovat.

11. Klepnutím na tlačítko **Uložit** uložte změny.
12. Zavřením stránky **Výchozí prognóza typu práce údržby**se vraťte na stránku **Výchozí nastavení typu práce údržby**.
13. Vyberte **Kontrolní seznam údržby**.
14. Na stránce **Kontrolní seznam výchozích nastavení typu práce údržby** můžete přidat řádky kontrolního seznamu údržby do vybraného výchozího typu práce údržby. Na záložce s náhledem **Řádky kontrolního seznamu údržby** možností **Nový** přidejte řádek kontrolního seznamu údržby.

    Čísla řádků se automaticky zadávají do pole **Číslo řádku** a označují posloupnost řádků kontrolního seznamu údržby. Čísla řádků lze podle potřeby upravovat. Po vytvoření prvního řádku kontrolního seznamu údržby vyberte řádek a stisknutím **klávesy se šipkou dolů** přidejte řádek pod ním. Případně můžete vybrat řádek kontrolního seznamu údržby a poté vybrat možnost **Nový**. V takovém případě bude nad vybraný řádek kontrolního seznamu údržby přidán nový řádek.

15. V poli **Typ** vyberte typ řádku a poté přidejte informace související s typem kontrolního seznamu údržby. Popis dostupných typů a souvisejících polí naleznete v oddílu [Vytvoření šablony kontrolního seznamu údržby](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Chcete-li zkopírovat nastavení kontrolního seznamu údržby z jiného typu práce údržby, vyberte možnost **Kopírovat kontrolního seznamu údržby** a poté vyberte typ práce údržby, ze kterého se má nastavení zkopírovat.
    >
    > Šablonu lze snadno vytvořit ze stávajícího kontrolního seznamu údržby. Šablonu pak můžete opakovaně používat v různých kontrolních seznamech údržby. Nová šablona bude přesnou kopií aktivního kontrolního seznamu údržby. Vyberte **Vytvořit šablonu** a poté zadejte název šablony. Chcete-li nahradit stávající kontrolní seznam údržby jedním řádkem, který odkazuje na novou šablonu, nastavte volbu **Nahradit** na hodnotu **Ano**. Obsah šablony lze zobrazit na stránce podrobností pro **Šablony kontrolního seznamu údržby**.

16. Klepnutím na tlačítko **Uložit** uložte změny.
17. Vraťte se na stránku **Výchozí hodnoty typu práce údržby**.
18. Vyberte možnost **Nástroje**.
19. Na stránce **Výchozí nástroje typu práce údržby** můžete přidat nástroje (prostředky), které chcete použít pro typ práce údržby. Vyberte možnost **Nový** a poté v poli **Prostředek** vyberte potřebný nástroj.

    > [!NOTE]
    > Chcete-li zkopírovat nastavení nástroje z jiného typu práce údržby, vyberte možnost **Kopírovat nástroje** a poté vyberte typ práce údržby, ze kterého se má nastavení zkopírovat.

20. Klepnutím na tlačítko **Uložit** uložte změny.
21. Vraťte se na stránku **Výchozí hodnoty typu práce údržby**.
22. Vyberte **Popisu práce**.
23. Na stránce **Popis práce** vyberte možnost **Upravit** a poté dle potřeby přidejte popis související s vybraným výchozím nastavením typu práce údržby.
24. Kliknutím na tlačítko **Uložit** uložte popis.

    Přidáte-li sem popis práce, dojde k přepsání veškerého popisu, který je nastaven pro typ práce údržby na stránce **Typy práce údržby**. Pokud zde nepřidáte popis práce, použije se jakýkoliv popis, který je nastaven pro typ práce údržby. Popisy jsou automaticky převedeny do pracovních příkazů, které používají typ práce údržby nebo výchozí typ práce údržby.

25. Vraťte se na stránku **Výchozí hodnoty typu práce údržby**.
26. Chcete-li nastavit přílohy pro vybraný výchozí řádek typu práce údržby, vyberte možnost **Připojit dokumenty**. Přílohy nastavené pro výchozí řádek typu práce údržby jsou automaticky zahrnuty na řádcích pracovního příkazu, které používají tento výchozí řádek typu práce údržby.
27. Vyberte **Nový** a poté vyberte typ dokumentu.
28. Nahrajte dokument nebo soubor.
29. Na stránce **Přílohy** nastavte pole. Nastavení přílohy používá standardní funkce nastavení dokumentu v aplikaci Microsoft Dynamics 365 for Finance and Operations.
30. Kliknutím na tlačítko **Uložit** uložte přílohu.

    > [!NOTE]
    > Přílohy pro výchozí řádek typu práce údržby jsou vytištěny společně se sestavou pracovního příkazu pouze v případě, že jsou na kartě **Typy dokumentů** na stránce **Parametry správy majetku** vybrány typy dokumentů (**Správa majetku** \> **Nastavení** \> **Parametry správy majetku**). Příklady příloh obsahujících pokyny, které vysvětlují, jak provést určitou úlohu nebo předdefinovaný kontrolní seznam údržby (pokud nepoužíváte funkci kontrolního seznamu údržby pro výchozí řádky typu práce údržby).

    Na stránce **Výchozí nastavení typu práce údržby** zobrazuje každý řádek počet prognózovaných hodin a také počet řádků, které byly vytvořeny pro položky, výdaje, kontrolní seznamy údržby a nástroje. Pole **Majetek** zobrazuje počet aktivních položek majetku, které souvisí s výchozím řádkem typu práce údržby.

31. Chcete-li zkopírovat výchozí typ práce údržby do jiného typu práce údržby, vyberte výchozí řádek typu práce údržby, do kterého se má kopírovat další nastavení, vyberte možnost, **Kopírovat nastavení** a poté vyberte výchozí typ práce údržby, který chcete kopírovat.
32. Chcete-li zobrazit seznam majetku, plánů údržby nebo pořadí údržby, které aktuálně používají výchozí řádek typu práce údržby, vyberte tento řádek a pak vyberte položku **Používá**.

![Obrázek č. 7](media/07-setup-for-work-orders.png)

Když systém vybere dostupný výchozí typ práce údržby, který se má použít na řádku pracovního příkazu, výběr bude založen na majetku a na nastavení souvisejícího typu majetku. Správa majetku projde všechny výchozí záznamy typu práce údržby, které souvisejí s typem práce údržby, který souvisí s typem majetku a zkontroluje možné shody. Vždy zkontroluje nejdříve nejkonkrétnější kombinaci. Jinými slovy, aby bylo možné najít co nejkonkrétnější kombinace, modul Správa majetku nejprve zkontroluje možné shody v poli **Obor**. Pokud není nalezena shoda, zkontroluje shodu v poli **Varianta typu práce údržby**. Pokud není nalezena žádná shoda, aplikace hledá shodu pro pole **Typ práce údržby** a tak dále (**Obor**, poté **Varianta typu práce údržby**, poté **Typ práce údržby**, poté **Majetek**, poté **Model**, poté **Výrobce** a poté **Typ majetku**). Není-li nalezena žádná shoda, použije se výchozí záznam, v němž je vybrán pouze typ práce údržby.

ID aktivity projektu automaticky souvisí s jednotlivými výchozími řádky typu práce údržby, které vytvoříte. Aktivita projektu je vytvořena v projektu prognózy, který je vybrán v poli **Projekt prognózy údržby** na kartě **Majetek** na stránce **Parametry správy majetku**. Účelem aktivity projektu je spravovat prognózy podle hodin, položek a výdajů ve vztahu k pracovním příkazům. Prognózy typu práce údržby se automaticky přenesou do řádku pracovního příkazu a zkopírují se z projektu prognózy do projektu pracovního příkazu, který je vytvořen pro řádek pracovního příkazu. Účelem aktivity projektu je spravovat prognózy ve vztahu k pracovním příkazům.

Můžete nastavit dávkovou úlohu pro aktualizaci výchozích odkazů typu práce údržby v pravidelných intervalech, nebo můžete úlohu spustit ručně. Chcete-li vytvořit dávkovou úlohu, nebo spustit ruční aktualizaci, vyberte **Správa majetku** \> **Pravidelně** \> **Preventivní údržba** \> **Aktualizovat výchozí odkazy typu práce údržby**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Přehled typů práce údržby, které souvisejí s majetkem

Po vytvoření požadovaných výchozích kombinací typů práce údržby můžete na stránce **Všechen majetek** získat přehled o aktuálním typu práce údržby, který souvisí s konkrétním majetkem. Přehled zobrazuje všechny výchozí kombinace typu práce údržby, které lze použít pro typ majetku vybraný pro daný majetek. Tyto kombinace zahrnují varianty typů práce údržby a obory práce údržby.

1. Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.
2. V seznamu vyberte majetek, pro který chcete zobrazit přehled kombinací typů práce údržby.
3. V podokně akcí na kartě **Obecné** vyberte skupinu **Související informace** a poté **Typy práce údržby**.

    V levém podokně na stránce **Typy práce údržby majetku** se zobrazí seznam všech kombinací typů práce údržby, které souvisejí s vybraným majetkem.

4. Výběrem kombinace typů práce údržby zobrazíte související nastavení pro kontrolní seznamy údržby, prognózy a nástroje. V části **Podrobnosti** na záložce s náhledem **Výchozí nastavení typu práce údržby** se zobrazuje počet souvisejících kontrolních seznamů údržby, prognózované hodiny, položky atd., které souvisejí s vybranou kombinací typů práce údržby.
5. Chcete-li zobrazit podrobnosti pro vybraný typ práce údržby, vyberte možnost **Typy práce údržby**.

![Obrázek č. 8](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Automatická aktualizace prognóz typu práce údržby

V modulu Správa majetku můžete automaticky aktualizovat všechny změny typu práce údržby. prognózy pro hodinové náklady, náklady na položky a výdaje, které byly aktualizovány v jiných modulech aplikace Finance and Operations. Tímto způsobem pomůžete zaručit, že prognózy typů práce údržby vždy používají nejaktuálnější nákladové ceny.

1. Vyberte možnosti **Správa majetku** \> **Pravidelně** \> **Prognóza** \> **Aktualizovat prognózu typu práce údržby**.
2. V dialogovém okně **Aktualizovat prognózu typu práce údržby** na záložce s náhledem **Záznamy k zahrnutí** můžete dle potřeby přidat výběr pro konkrétní typy práce údržby. Vyberte **Filtr** a poté volbou **Vybrat** proveďte výběr.
3. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.
4. Kliknutím na tlačítko **OK** spustíte aktualizaci prognózy.
