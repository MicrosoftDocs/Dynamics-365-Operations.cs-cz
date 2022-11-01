---
title: Automatizace vyrovnání hlavní knihy
description: V tomto článku jsou informace o procesu automatizace vyrovnání hlavní knihy.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708325"
---
# <a name="automate-ledger-settlements"></a>Automatizace vyrovnání hlavní knihy

[!include [banner](../includes/banner.md)]

V Microsoft Dynamics 365 Finance verze 10.0.31 je funkce  **Proces automatizace vyrovnání hlavní knihy** k dispozici v pracovním prostoru  **Správa funkcí** . Funkci **Automatizovat proces vypořádání hlavní knihy** můžete zapnout pouze v případě, že byla funkce **Povědomí mezi vypořádáním účetní knihy a uzávěrkou na konci roku** zapnuta.

Vyrovnání hlavní knihy je proces spárování transakce Má dáti a Dal v hlavní knize. Organizace, které provádějí činnosti vypořádání hlavní knihy podle opakovaného plánu, mohou nyní tento proces automatizovat. Během procesu automatického vypořádání hlavní knihy lze automaticky spárovat debetní transakci a kreditní transakci pouze v případě, že se jejich částky v účetní měně rovnají.Například debetní částka 1,00 USD může být automaticky spojena s kreditní částkou 1,00 USD. Debetní hodnotu 1,00 USD však nelze automaticky přiřadit ke dvěma kreditům, z nichž každý má hodnotu 0,50 USD. Částečné spárování částek transakcí hlavní knihy není podporováno.

Automatizace vypořádání hlavní knihy definuje následující údaje:

- Když jsou spuštěna vypořádání hlavní knihy
- Jaká kritéria se používají pro spárování debetů a kreditů, které lze automaticky vypořádat
- V jakém pořadí jsou zpracovávány informace o vypořádání hlavní knihy

## <a name="define-the-occurrence-of-ledger-settlements"></a>Definice výskytu vypořádání hlavní knihy

Automatizace vypořádání účetních knih používá rámec automatizace procesů. Různé obchodní procesy používají tento systém k definování opakování vybraného procesu. Pro vypořádání hlavní knihy přejděte na  **Správa systému \> Nastavení \> Automatizace procesu** nebo **Hlavní kniha \> Nastavení hlavní knihy \> Automatizace procesu**.

Nejprve vyberte možnost  **Vytvořit novou automatizaci procesu** a vyberte  **Vypořádání hlavní knihy**. Průvodce vás provede procesem nastavení automatizace.

## <a name="general-page"></a>Stránka Obecné

Na stránce průvodce  **Obecné**  zadejte název výskytu vypořádání hlavní knihy, který vytváříte. Pokud jsou například vaše odpovídající debety a kredity zúčtovány v pondělí, zadejte popisný název, např.  **LedgerSettle\_Mon**. Název, který zadáte, se zobrazí ve sloupci **Pravidlo automatizace** na stránce  **Vypořádání hlavní knihy** .

Zbývající nastavení na stránce jsou obecná a definují vzor výskytu pro tuto verzi návrhu vypořádání hlavní knihy. Pokud je například výskyt pro pondělí, můžete jej definovat tak, aby se spouštěl každý týden, a můžete vybrat pondělí jako den v týdnu, kdy se spustí. Můžete také zadat čas předběžného plánu, například 14:00, takže automatizace procesů bude dokončena před začátkem následujícího pracovního dne. Doporučujeme naplánovat automatizaci procesů tak, aby byla prováděna mimo vaši běžnou pracovní dobu. Tímto způsobem pomůžete snížit dopad na vaše účetní během pracovního dne.

Pro více informací o ostatních polích na stránce  **Obecné**  viz dokumentace k automatizaci procesů.

## <a name="ledger-settlements-match-criteria-page"></a>Stránka Kritéria shody vyrovnání hlavní knihy

Další stránka v průvodci je stránka  **Kritéria shody vyrovnání hlavní knihy** . Používá se k definování hlavních účtů, které jsou zahrnuty do výskytu automatizace procesů, a kritérií, která se používají k určení odpovídajících debetů a kreditů.

### <a name="account-selection"></a>Výběr účtu

Zobrazí se hlavní účty, které jste dříve definovali jako účty vypořádání hlavní knihy pro právnickou osobu. (Definujete hlavní účty jako účty vyrovnání hlavní knihy v nastavení **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy \> Vypořádání hlavní knihy**.)

### <a name="main-account-and-posting-layer"></a>Hlavní účet a účtovací vrstva

Hodnoty  **Hlavní účet** a **Účtovací vrstva**  jsou povinná kritéria shody. Hodnoty **Hlavní účet** a **Účtovací vrstva** debetní a kreditní transakce v hlavní knize musí mít být stejné, aby mohly být spárovány během procesu automatického vyrovnání hlavní knihy.

### <a name="posting-type"></a>Typ zaúčtování

Možnost **Typ zaúčtování** vyberte, pokud debetní a kreditní transakce v hlavní knize musí mít stejný typ zaúčtování, aby mohly být spárovány během procesu automatického vyrovnání hlavní knihy.

### <a name="financial-dimensions"></a>Finanční dimenze

Možnost **Finanční dimenze** vyberte, pokud debetní a kreditní transakce v hlavní knize musí mít stejné finanční dimenze, aby mohly být spárovány během procesu automatického vyrovnání hlavní knihy. Když je vybrána tato možnost, kritéria pro hodnoty finanční dimenze musí být vybrána v seznamu **Dostupné finanční dimenze**. Seznam **Dostupné finanční dimenze** neobsahuje hlavní dimenzi účtu, protože je automaticky vyžadována jako součást kritérií shody.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Zobrazení výsledků automatizace vyrovnání hlavní knihy

Po vytvoření řady automatizace vyrovnání hlavní knihy jsou výskyty pro každé vypořádání hlavní knihy zobrazeny v týdenním zobrazení automatizace procesů. Dále je zobrazen stav každého výskytu. Jsou použity následující stavy:

- **Naplánováno**  – Automatizace je naplánována, ale dosud nebyla spuštěna.
- **Provádění** – Automatizace právě běží.
- **Chyba**  – Automatizace byla spuštěn, ale došlo k chybě. Chyby si můžete prohlédnout výběrem tlačítka  **Zobrazit výsledky** .
- **Dokončeno**  – Automatizace byla úspěšně spuštěna. Výsledky vypořádání si můžete prohlédnout na stránce **Vyrovnání hlavní knihy**.

Chcete-li zobrazit odpovídající výsledky, přejděte na **Hlavní kniha \> Periodické úkoly \> Vyrovnání hlavní knihy**. Pole **Pravidlo automatizace** na stránce **Vyrovnání hlavní knihy** zobrazuje název automatické naplánované úlohy vypořádání hlavní knihy, která byla použita k vypořádání transakce. Neúspěšné pokusy o vyrovnání neaktualizují hodnotu **Pravidlo automatizace**. Pokud ručně stornujete transakci, která byla dříve úspěšně vypořádána procesem automatizace, hodnota **Pravidlo automatizace** bude odstraněno.

Pole **Datum vyrovnání** pro spárované záznamy zobrazuje datum, kdy byl proces automatizace proveden.

## <a name="editing-a-ledger-settlement-automation"></a>Úprava automatizace vyrovnání hlavní knihy

Systém automatizace procesů vám umožňuje upravit řadu a výskyty, které jsou vytvořeny pro vyrovnání hlavní knihy. Řadu lze upravit buď na stránce  **Automatizace procesů**  nebo v týdenním zobrazení automatizace procesů. Pokud se například správce závazků rozhodne provést vypořádání hlavní knihy ve středu místo v pondělí, může najít událost v týdenním zobrazení a vybrat  **Zobrazit/Upravit – Řada**.

Pokud upravíte řadu, jste vyzvání k zadání, zda by se měla změna provést u všech existujících výskytů, nebo pouze u nových výskytů. Historické události, které již mají stav **Dokončeno** nebo skončily stavem  **Chyba** , se nezmění.

Můžete také přidat nový výskyt nebo změnit existující výskyt. Například další výskyt vypořádání hlavní knihy je naplánován na středu 1. ledna, ale toto datum je svátek. Výskyt můžete změnit na stránce  **Automatizace procesů**  nebo z týdenního zobrazení automatizace procesů. Otevře se stránka, která zobrazuje podrobnosti plánu a kritéria párování. Zde můžete upravit plánovaný čas a datum. V případě potřeby můžete také upravit kritéria párování. 

Můžete také zakázat výskyt nebo řadu. Chcete-li deaktivovat výskyt a pozastavit jeho zpracování, vyberte jej v týdenním zobrazení automatizace procesů a poté vyberte  **Deaktivovat**. Řadu můžete deaktivovat na stránce **Automatizace procesů** .

## <a name="security-for-ledger-settlement-automation"></a>Zabezpečené automatizace vyrovnání hlavní knihy

Úloha **Udržovat nastavení řady automatizace vyrovnání hlavní knihy** byla přidána k rolím vedoucího účetnictví a vedoucího účetnictví a role **Zobrazit nastavení řady automatizace vyrovnání hlavní knihy** povinnost byla přidána do rolí Účetní, Účetní manažer a Vedoucí účetnictví pro automatizaci vyrovnání hlavních knih. Tyto úkoly jsou výchozím nastavením zabezpečení, ale lze je změnit na základě požadavků vaší organizace.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Parametry hlavní knihy pro automatizaci vyrovnání hlavní knihy

Pole **Typický zůstatek vypořádání** označuje pořadí, ve kterém bude zpracováno automatické zúčtování hlavní knihy. Chcete-li nastavit nebo zobrazit hodnotu **Typický zůstatek vypořádání**, přejděte na **Hlavní kniha \> Nastavení \> Parametry hlavní knihy** a vyberte kartu **Vyrovnání hlavní knihy**.

Pokud je vybrána možnost **Debetní**, proces automatizovaného vyrovnání hlavní knihy začne na straně debetu a hledá odpovídající kredity. Pokud je vybrána možnost **Kreditní**, proces automatizovaného vyrovnání hlavní knihy začne na straně kreditu a hledá odpovídající debety. Tato možnost by měla odrážet typický zůstatek hlavního účtu.

## <a name="processing-a-ledger-settlement-automation"></a>Zpracování automatizace vyrovnání hlavní knihy

Když je automatizace spuštěna, systém vybere transakce hlavní knihy pro hlavní účty, které jsou definovány pro řadu automatizace procesů. Seřazuje transakce podle data pomocí časového rozsahu od začátku fiskálního roku do data, kdy je spuštěna automatizace procesu. Páruje na základě zadaných kritérií shody. Absolutní hodnoty částek v účetní měně debetu a kreditu se musí shodovat, aby mohly být vypořádány.

Zatímco hlavní účet je zpracováván výskytem automatizace vyrovnání hlavní knihy, nemůžete ho zobrazit na stránce **Vyrovnání hlavní knihy**. Musíte počkat na dokončení procesu automatizace. Doporučujeme naplánovat spuštění automatizace procesů mimo pracovní dobu, abyste předešli konfliktům.

Proces automatizace bude zahrnovat všechny transakce, které splňují kritéria, kromě transakcí, které byly ručně označeny k vypořádání na stránce **Vypořádání hlavní knihy**.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Storno transakcí, které jsou vypořádány procesem automatizace

Vyrovnání provedení procesem automatizovaného vyrovnání hlavní knihy lze stornovat. Pokud stornujete transakci, která byla dříve vypořádána procesem automatizace, hodnota **Pravidlo automatizace** bude odstraněno.
