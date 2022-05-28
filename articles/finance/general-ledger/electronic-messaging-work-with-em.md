---
title: Práce s funkcemi elektronických zpráv
description: Toto téma poskytuje informace o tom, jak pracovat s funkcí elektronických zpráv (EM).
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a65971fa1da60b00bb525d450c0eb59aee57116e
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733756"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Práce s funkcemi elektronických zpráv

[!include [banner](../includes/banner.md)]

Při práci na úrovni zprávy je užitečnější stránka **Elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Elektronické zprávy**). Při práci na úrovni sbírání dat nebo položek zprávy je užitečnější stránka **Položky elektronické zprávy** (**Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Položky elektronické zprávy**).

## <a name="electronic-messages"></a>Elektronické zprávy

Stránka **Elektronické zprávy** představuje zpracování, které je vám dostupné na základě vaší role. Role zabezpečení jsou přidruženy ke zpracování v jeho nastavení. Pro každé zpracování, které je vám k dispozici, stránka zobrazuje elektronické zprávy a informace, které s nimi souvisejí.

Pevná záložka **Zprávy** zobrazuje elektronické zprávy pro vybrané zpracování. V závislosti na stavu vybrané zprávy a předdefinovaném zpracování můžete některé akce provést výběrem tlačítek nad mřížkou:

- **Nový** – Toto tlačítko je přidruženo k akcím typu **Vytvoření zprávy**.
- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené zprávy.
- **Shromažďovat data** -Toto tlačítko je přidružen k akcím typu **Naplnit záznamy**.
- **Generovat sestavu** – Toto tlačítko je přidruženo k akcím typu **Zpráva exportu elektronického výkaznictví**.
- **Odeslat sestavu** – Toto tlačítko je přidruženo k akcím typu **Webová služba**.
- **Importovat odezvu** – Toto tlačítko je přidruženo k akcím typu **Import elektronického výkaznictví**.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele na úrovni zprávy**.
- **Položky zprávy** – Otevřete stránku **Pokožky elektronické zprávy**.

Záložka s náhledem **Protokol akce** zobrazuje informace o všechny akcích spuštěných pro vybranou zprávu. Pokud akce způsobila chybu, budou informace o chybě připojeny k příslušnému řádku protokolu akcí. Podrobné informace o chybě zobrazíte tak, že vyberete v mřížce řádek a vyberete tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

Záložka s náhledem **Další pole zprávy** zobrazuje všechna další pole, která jsou definována pro zprávy v nastavení zpracování. Na pevné záložce jsou zde uvedeny hodnoty těchto polí.

Záložka s náhledem **Položky zprávy** zobrazuje všechny položky zpráv související s vybranou zprávou. V závislosti na stavu vybrané položky zprávy a předdefinovaném zpracování můžete některé akce provést výběrem tlačítek nad mřížkou:

- **Odstranit** – Toto tlačítko je dostupné tehdy, pokud je zaškrtávací políčko **Povolit odstranění** vybráno pro aktuální stav zvolené položky zprávy.
- **Aktualizovat stav** – Toto tlačítko je přidruženo k akcím typu **Zpracování uživatele**.
- **Původní dokument** - Otevřete stránku obsahující původní dokument pro vybranou položku zprávy.

Sestavy, které již byly generovány a přijaty pro zprávu, jsou připojeny k této zprávě. Pokud chcete zobrazit přílohy související se zprávou, vyberte zprávu a potom vyberte tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

![Tlačítko Příloha](media/attachment-icon.png)

Stránka **Přílohy** zobrazuje přílohy, které souvisí s vybranou zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

![Tlačítko Otevřít](media/open-button.png)

Můžete zkontrolovat přílohy, které se vztahují k určité akci, která byla provedena u předchozí zprávy. Na stránce **Elektronické zprávy** na pevné záložce **Zprávy** vyberte zprávu. Na pevné záložce **Protokol akcí** vyberte akci a poté vyberte tlačítko **Příloha** (symbol sponky) v pravém horním rohu stránky.

Můžete spustit celé zpracování nebo pouze určitou akci výběrem možnosti **Spustit zpracování** v podokně akcí.

## <a name="electronic-message-items"></a>Položky elektronické zprávy

Stránka **Položky elektronické zprávy** obsahuje všechny položky zprávy a protokol akcí, které byly spuštěny pro každou položku zprávy. Stránka také zobrazuje také další pole definovaná pro položky zprávy a hodnoty těchto dalších polí.

Následující tabulka popisuje pole na kartě **Položky zprávy**.

<table>
<thead>
<tr>
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Zpracování</td>
<td>Název zpracování použitý k vytvoření položky zprávy.</td>
</tr>
<tr>
<td>Položka zprávy</td>
<td>ID položky zprávy. Toto ID je přiřazeno automaticky na základě číselné řady <b>Položky zprávy</b>, která je definována na stránce <b>Parametry hlavní knihy</b>.</td>
</tr>
<tr>
<td>Datum položky zprávy</td>
<td>Datum vytvoření položky zprávy.</td>
</tr>
<tr>
<td>Typ položky zprávy</td>
<td>Typ položky zprávy. Několik typů položek zpráv lze nastavit pro stejné zpracování (například <b>Příchozí faktury</b> a <b>Odchozí faktury</b>). Toto pole může být nastaveno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Stav položky zprávy</td>
<td><p>Skutečný stav položky zprávy. Dostupné stavy se liší v závislosti na typu položky zprávy. Několik příkladů:</p>
<ul>
<li><b>Naplněno</b> – Záznam byl přidán do tabulky položek zprávy.</li>
<li><b>Vyhodnoceno</b> – Další atributy byly vypočteny pro položku zprávy.</li>
<li><b>Vykázáno</b> – Položka zprávy byla úspěšně přidána do sestavy.</li>
<li><b>Vyloučeno</b> – Tento stav lze využít, pokud je třeba vyloučit některé položky zprávy ze sestavy před jejich exportem.</li>
</ul>
</td>
</tr>
<tr>
<td>Datum přenosu</td>
<td>Pro zpracování, které automaticky přenáší vygenerovanou sestavu mimo systém, je to datum, kdy byla položka zpráva přenesena.</td>
</tr>
<tr>
<td>Číslo dokumentu</td>
<td>Toto pole se nastaví automaticky na základě nastavení akce naplnění záznamů. Toto pole může být nastaveno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Číslo účtu</td>
<td>Číslo účtu odběratele nebo dodavatele (nebo jiná hodnota pole, v závislosti na poli, které je definováno pro akci Naplnit záznamy). Toto pole může být nastaveno automaticky pouze v případě, že je faktura přidána do tabulky položek zprávy.</td>
</tr>
<tr>
<td>Zpráva</td>
<td>Číslo zprávy. Toto číslo je přiřazeno automaticky na základě číselné řady <b>Zpráva</b>, která je definována na stránce <b>Parametry hlavní knihy</b>.</td>
</tr>
<tr>
<td>Stav zprávy</td>
<td>Skutečný stav elektronické zprávy.</td>
</tr>
<tr>
<td>Další akce</td>
<td>Další akce, které lze spustit pro aktuální stav položky zprávy.</td>
</tr>
</tbody>
</table>

Karta **Další pole** zobrazuje další pole pro vybranou položku zprávy a jejich hodnoty.

### <a name="run-processing"></a>Spustit zpracování

Vyberte **Spustit zpracování** v podokně akcí a spustíte zpracování pro položky zprávy. Ke spuštění určité akce nastavte v dialogovém okně **Spustit zpracování** možnost **Zvolit akci** na **Ano** a pak vyberte akci. Ke spuštění celého zpracování ponechte možnost **Zvolit akci** nastavenou na **Ne**.

### <a name="generate-report"></a>Generovat sestavu

V podokně Akce klikněte na možnost **Generovat sestavu**. Toto tlačítko je přidruženo k akcím typu **Export elektronického výkaznictví**.

### <a name="update-status"></a>Aktualizovat stav

Vyberte **Aktualizovat stav** v podokně akcí pro aktualizaci stavu jedné nebo více položek zprávy. V dialogovém okně **Aktualizovat stav** použijte záložku s náhledem **Záznamy k zahrnutí** a vyberte položky zprávy pro aktualizaci. Ujistěte se, že jste správně definovali kritéria výběru, protože stavy položky zprávy budou aktualizovány podle těchto kritérií, počátečního stavu vybrané akce a hodnoty, kterou zadáte do pole **Nový stav**. Po dokončení aktualizace stavu bude obtížné určit, které položky byly právě aktualizovány. Proto bude obtížné vrátit zpět aktualizaci stavu.

### <a name="electronic-messages"></a>Elektronické zprávy

Vyberte **Elektronické zprávy** v podokně akcí a zkontrolujte elektronickou zprávu, která souvisí s vybranou položkou zprávy.

Můžete také zkontrolovat soubory, které odpovídají konkrétní položce zprávy. Vyberte pole **Zpráva** položky zprávy nebo vyberte **Elektronické zprávy** v podokně akcí. Na stránce **Elektronická zpráva** vyberte zprávu, jejíž soubory chcete zkontrolovat, a potom vyberte tlačítko **Příloha** (ikona papírové spony) v pravém horním rohu stránky.

Stránka **Přílohy** zobrazuje přílohy, které souvisí se zprávou. Pokud chcete zobrazit soubor, vyberte ho ze seznamu vlevo a poté vyberte **Otevřít** v podokně akcí.

### <a name="original-document"></a>Původní dokument

Vyberte **Původní dokument** v podokně akcí a otevřete původní dokument pro vybranou položku zprávy.
