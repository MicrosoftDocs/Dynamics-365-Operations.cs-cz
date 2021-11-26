---
title: Vytváření dokumentace nebo školení pomocí záznamníku úloh
description: Toto téma vysvětluje, co je Záznamník úkolů a průvodci záznamem úloh, jak vytvořit nahrávky a jak přizpůsobit průvodce záznamem úloh Microsoft a zahrnout je do nápovědy.
author: josaw1
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d137b5dbde52423d0e040c3012fb4f1eee2368d4
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781225"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Vytváření dokumentace nebo školení pomocí záznamníku úloh

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, co je Záznamník úkolů a průvodci záznamem úloh, jak vytvořit nahrávky úkolů a jak přizpůsobit průvodce záznamem úloh Microsoft a zahrnout je do nápovědy.

> [!IMPORTANT]
> Můžete nahrát své vlastní průvodce záznamem úloh pro aplikaci Dynamics 365 Human Resources, ale nebude možné je uložit do knihovny modelování podnikových procesů nebo je otevřít z podokna Nápovědy. Můžete je uložit v místním počítači nebo na umístění v síti a potom je otevřít a přehrát pomocí záznamníku úkolů. 

## <a name="learn-about-task-recorder"></a>Informace o Záznamníku úkolů

Záznamník úkolů je nástroj, který umožňuje zaznamenat akce prováděné v uživatelském rozhraní produktu. Při použití Záznamníku úkolů jsou zaznamenány všechny události prováděné v uživatelském rozhraní, které jsou spouštěny na serveru, včetně přidání hodnot, změny nastavení a odebrání dat. Kroky, které zaznamenáte, jsou souhrnně označovány termínem *záznam úkolu*. Záznamy úloh lze používat mnoha způsoby:

-   **Záznamy úkolů lze přehrát jako průvodce úkolem.** Průvodci záznamem úloh jsou nedílnou součástí prostředí nápovědy. Průvodce záznamem úloh je kontrolovaný, řízený a interaktivní způsob, který vás provede kroky daného úkolu nebo obchodního procesu. Uživatel obdrží pokyny k dokončení jednotlivých kroků pomocí je místních výzev (nebo "bublin"), která se zobrazí v uživatelském rozhraní a odkazují na prvek uživatelského rozhraní, který musí uživatel použít. Bublina obsahuje také informace o tom, jak pracovat s prvkem, jako je "Klepněte sem" nebo "Do tohoto pole zadejte hodnotu." Spouští se v rámci aktuální datové sady uživatele a dat, která jsou zadána a uložena v prostředí uživatele.
-   **Záznamy úkolů lze uložit jako dokumenty Word.** Tímto způsobem lze snadno vytvářet tisknutelné přepisy školení.

Můžete vytvořit vlastní záznamy úkolů, přehrávat záznamy úkolů poskytované společností Microsoft nebo upravovat záznamy úkolů poskytované společností Microsoft podle konfigurace. Další informace o Záznamníku úloh naleznete v tématu [Záznamník úloh](task-recorder.md).

## <a name="plan-your-task-recording"></a>Plánování záznamu úkolů
Při vytváření nového záznamu úkolů nebo založení záznamu na záznamů úkolů Microsoft mějte na paměti následující informace.

-   Naplánujte záznam jako video. Proveďte všechna rozhodnutí dopředu.
-   Projděte si obchodní proces jednou nebo dvakrát bez záznamu, abyste se seznámili s jednotlivými kroky.
-   Při procházení procesu před záznamem si všimněte, kde se používají klávesové zkratky nebo klávesa **Enter**, abyste se vyhnuli jejich použití při skutečném záznamu.
-   Určete následující:
    -   Chcete seskupit kroky společně nebo do dílčích úkolů? Dílčí úkoly vizuálně oddělují části procesu. Chcete-li například vytvořit záznam pro „vytváření a vydání produktu“, možná budete chtít seskupit kroky, které jsou nutné k vytvoření produktu, a poté seskupit kroky, které jsou nutné k vydání produktu. Dílčí úkoly také usnadňují čtení delších procesů.
    -   Opravdu chcete přidávat poznámky? A pokud ano, kam? Další informace najdete v tématu "Seznámení s různými typy poznámek".
    -   Jaké hodnoty přidáte do různých polí, jakmile dokončíte kroky obchodního procesu? Doporučujeme vědět, co vyberte nebo zadáte během procesu, abyste se nemuseli vracet zpět a opravovat chyby při vytváření záznamů.

**Zapište si popis a poznámky dopředu**

-   Na začátku každého záznamu úkolu je popis pole, které slouží k zadání úvodu k záznamu. Doporučujeme zapsat a uložit si popis předem do samostatného dokumentu, abyste jej mohli zkopírovat a vložit do záznamu úkolů při jeho nahrávání. Tímto způsobem se můžete věnovat úpravě textu, pokud nejste v procesu záznamu. Vyjmutí a vložení textu urychlí a zjednoduší proces záznamu.
-   Pro každý krok při záznamu úkolu můžete vytvořit poznámky. Během přehrávání průvodce úkolem se poznámky zobrazí v "bublině" jako poznámky nad nebo pod textem kroku. Když poznámky prohlížíte jako text v podokně nápovědy, zobrazí se jako text vložený v kroku. Stejně jako v případě popisu doporučujeme zapsat a uložit poznámky do samostatného dokumentu. Při záznamu úkolu vyjměte a vložte poznámky z tohoto dokumentu.

**Seznámení s různými typy poznámek** Všechny poznámky jsou volitelné. Přidejte je, pouze když poskytují užitečné informace uživateli.

-   **Nadpis:** Poznámka k nadpisu se zobrazí za textem kroku, který Záznamník úkolů automaticky vygeneruje. V průvodci záznamem úloh se nadpis poznámky zobrazí nad automaticky generovaným textem. Použijte tento typ poznámek, chcete-li vysvětlit, proč uživatel provádí daný krok, nebo poskytnout další kontext.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Nadpis** zadejte poznámku k nadpisu. 

[![Podokno úprav s poznámkou v záhlaví.](./media/screen1.png)](./media/screen1.png) 

Toto je vzhled poznámky k nadpisu v bublině v průvodci záznamem úloh. 

[![Vzhled poznámky nadpisu v Průvodci záznamem úloh.](./media/screen2.png)](./media/screen2.png)

-   **Poznámky:** Poznámka k poznámkám se zobrazí za textem kroku, který Záznamník úkolů automaticky vygeneruje. V průvodci úkolem bude viditelná, pouze pokud uživatel klikne na odkaz **Zobrazit více** v bublině v průvodci úkolem. Použijte tento typ poznámky, chcete-li popsat cokoli, co musí uživatel znát pro dokončení kroku.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Poznámky** zadejte poznámku k poznámkám. 

[![Podokno úprav s komentářem v poli Poznámky.](./media/screen3.png)](./media/screen3.png) 

Toto je vzhled poznámky v bublině v průvodci záznamem úloh.

[![Vzhled anotace Poznámky v Průvodci záznamem úloh.](./media/screen4.png)](./media/screen4.png)

-   **Informační krok**: Tyto poznámky se vytvářejí kliknutím pravým tlačítkem na ovládací prvek nebo na libovolné místo ve formuláři &lt; **Záznamník úloh** &lt; **Přidat informační krok.** Informační kroky se zobrazují v jakémkoli kroku vložení, i když nebyla zaznamenána žádná akce v uživatelském rozhraní. Můžete přidat krok informací na úrovni formuláře nebo krok informací přidružený k ovládacímu prvku. Je-li krok informací přidružen k formuláři, zobrazí se "bublina" průvodce úkolem jinde ve formuláři, bez ukazatele, když je přehráván průvodce úkolem. Je-li informační krok přidružen k formuláři, bude "bublina" průvodce záznamem úloh odkazovat na ovládací prvek, kde se průvodce záznamem úloh přehrává. V podokně Nápověda se poznámka informačního kroku zobrazuje jako očíslovaný krok s jakýmkoli zadaným textem. Kroky informací slouží k přípravě uživatele na následující kroky, k popisu kroků, které je třeba provést mimo aplikaci, nebo pro účely odkazování na jiné záznamy (však v poznámkách nelze vytvořit hypertextové odkazy).

**Určete, jak dlouho budete záznam provádět**

-   Uživatel bude obecně číst nebo přehrávat záznam od začátku do konce, takže nekombinujte kroky nebo úkoly, které je lépe provádět samostatně.
-   Snažte se nevytvářet záznamy dlouhého scénáře, který zahrnuje více dílčích procesů. Například téma „Práce v oddělení služeb pro odběratele v obchodě“ je příliš široké. Rozdělte je na kratší úkoly, například „Přijmout vrácení“ a „Přidat k dárkovému poukazu“.
-   Pokud lze úkol provést v rámci několika různých obchodních procesů, vytvořte pro něj samostatný záznam. Můžete na něj odkázat v ostatních záznamech.
-   Pokud proces zahrnuje více úkolů, které osoba pravděpodobně provede najednou, lze úkoly uložit do jednoho záznamu, například "Nastavení a přiřazení profilů funkcí".
-   Pokud jde o něco, co uživatel udělá jednou (například konfigurace), a pak o další úkol, který může provést okamžitě po prvním, který se však provádí opakovaně a samotně, rozdělte je do dvou záznamů úkolů.

**Rozhodněte, kde v uživatelském rozhraní spustit nahrávání** Stránka, na kterou přejdete při spuštění nahrávání záznamu úkolu, ovlivní, pro kterou stránku se průvodce záznamem úloh přehraje. Například pokud chcete uvést záznam úlohy v podokně Nápověda při kliknutí na tlačítko Nápověda na stránce Parametry hlavní knihy, je nutné spustit nahrávání na stránce parametry hlavní knihy. **Uložte záznamy jako soubory AXT** Jakmile dokončíte vytvoření nebo úpravu záznamu úkolu, máte k dispozici několik možností pro stažení nebo uložení záznamu. Soubor lze stáhnout jako balíček záznamu úkolu (AXTR), jako neupravený soubor záznamu (XML) nebo jako dokument aplikace Word a uložit soubor do knihovny LCS. Je vhodné záznam úkolu vždy uložit jako souboru balíčku záznamu úkolů (AXTR). To vám usnadní údržbu souborů, pokud bude později nutné změnit postupy nebo poznámky. Chcete-li stáhnout soubor jako dokument aplikace Word, uložte jej také jako soubor balíčku záznamu úlohy.

## <a name="create-your-task-recording"></a>Vytvoření záznamu úkolu
Podrobný přehled kroků naleznete v tématu [Zdroje záznamníku úloh](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopírování a přizpůsobení záznamu úkolů společnosti Microsoft
Můžete stáhnout a upravovat záznamy úkolů společnosti Microsoft a použít je pro vlastní dokumentaci k nápovědě nebo výukové materiály. Při stažení záznamu úkolu Microsoft postupujte takto:

1.  Otevřete záznamník úloh. Záznamník úkolů se nachází v nabídce **Nastavení**.
2.  V podokně Záznamník úkolů klikněte na tlačítko **Udržovat záznam.**
3.  V části **Kde je záznam** klikněte na tlačítko **Nachází se v knihovně LCS**.
4.  Klikněte na možnost **Vybrat knihovnu LCS**.
5.  Vyberte globální knihovnu Microsoft.
6.  Ve stromovém zobrazení vyberte uzel knihovny obchodního procesu přidružený k záznamu úkolů.
7.  Klepněte na tlačítko **OK**.
8.  Klikněte na tlačítko **Spustit**.
9.  V tomto okamžiku procházejte záznam a změňte jakékoli kroky v průběhu nahrávání.. **Poznámka:**: Chcete-li pouze změnit text nahrávání, můžete otevřít záznam v režimu **úprava poznámky záznamu** režimu a potom ho uložit.
10. Po přehrání záznamu do konce klikněte na tlačítko **Zastavit** na panelu Záznamníku úkolů v horní části obrazovky.
11. Vyberte, jak chcete záznam úkolu uložit.



## <a name="additional-resources"></a>Další prostředky

[Systém nápovědy](../../fin-ops/get-started/help-overview.md)

[Připojení k systému nápovědy](../../fin-ops/get-started/help-connect.md)

[Záznamník úloh](task-recorder.md)

[Vytvořit témata nápovědy ve formátu RTF pomocí Záznamníku úkolů (externí odkaz)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]