---
title: Konfigurace kontrolorů výdajů
description: Toto téma popisuje, jak pomocí kontrolorů výdajů dynamicky vybrat uživatele, kterému je přiřazen úkol pracovního postupu, schválení nebo ruční rozhodnutí.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070139"
---
# <a name="configure-expenditure-reviewers"></a>Konfigurace kontrolorů výdajů
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Dynamické kontrolory výdajů můžete nastavit na směrování výdajů ke kontrole podle uživatele, který je přiřazen k roli projektu, nebo finanční dimenze, kde jsou výdaje účtovány. Proces workflowu používá zadanou roli projektu nebo vlastníka finanční dimenze k určení, komu mají být výdaje směřovány.

Při vytváření pracovního postupu můžete definovat jednu nebo více konfigurací kontrolora výdajů a potom vybrat konfiguraci. Můžete nakonfigurovat hodnoty recenzenta výdajů pro každou právnickou osobu ve vaší organizaci. Po definování konfigurací kontrolora výdajů přiřaďte konfiguraci. Kontrolorům výdajů lze přiřadit úkoly pracovního postupu, schválení a manuální rozhodnutí.

> [!NOTE]
> I když recenzenti výdajů nejsou povinní, mohou pomoci zjednodušit konfiguraci vašeho pracovního postupu. Například nemusíte vytvářet jedno podmíněné rozhodnutí, abyste zkontrolovali každou dimenzi nákladového střediska, a pak vytvořit další prvek, který přiřadí schválení nebo úkol konkrétnímu uživateli nebo skupinám uživatelů. Místo toho můžete nakonfigurovat vlastníka dimenze nákladového střediska a použít kontrolora výdajů k dynamickému výběru správného uživatele. Tímto způsobem, když se změní vlastnictví nebo přiřazení nákladových středisek, stačí aktualizovat pole **Majitel** pro finanční dimenzi.

## <a name="types-of-expenditure-reviewers"></a>Typy recenzentů výdajů

Ne všechny pracovní postupy podporují koncept kontrolorů výdajů. Ve výchozím nastavení můžete nakonfigurovat kontrolory výdajů pro nákupní žádankt, nákupní objednávky, faktury dodavatele a sestavy výdajů. Každý z těchto typů pracovních postupů vyžaduje, abyste nakonfigurovali kontrolory výdajů na samostatné stránce, která je specifická pro funkci a modul. U každého podporovaného dokumentu lze kontrolory výdajů použít buď s pracovními postupy na úrovni záhlaví, nebo s pracovními postupy na úrovni řádků.

Následující tabulka ukazuje, kam přejdete ke konfiguraci kontrolora výdajů pro každý podporovaný dokument.

| Doklad | Navigační cesta |
|----------|-----------------|
| Sestavy výdajů | Správa výdajů \> Nastavení \> Zásady \> Kontroloři výdajů |
| Nákupní objednávky | Zásobování a získávání zdrojů \> Nastavení \> Zásady \> Recenzenti výdajů nákupních objednávek |
| Nákupní žádanky | Zásobování a získávání zdrojů \> Nastavení \> Zásady \> Recenzenti výdajů nákupních žádanek |
| Faktury dodavatele | Závazky \> Nastavení zásad \> Kontroloři výdajů faktur dodavatele |

## <a name="expenditure-reviewer-assignments"></a>Přiřazení kontrolora výdajů

Pro každého recenzenta výdajů jsou k dispozici dva typy přiřazení: *distribuce projektu* a *distribuce organizace*. U distribuce projektu si můžete vybrat mezi autoritami projektu a finančními dimenzemi. Pro distribuci organizace můžete vybrat finanční dimenze.

Mezi autority projektu patří projektový manažer, správce projektu a manažer prodeje projektu. Tato oprávnění definujete přímo ve svém projektu výběrem pracovníka v příslušných polích.

Finanční dimenze jsou řízeny strukturami účtů v každé právnické osobě. U každé právnické osoby můžete vybrat, které finanční dimenze budou použity u kontrolora výdajů. Dimenze mohou pocházet buď z projektu (v tomto případě vyberete dimenze na kartě **Distribuce projektu**), nebo dokumentu (v tomto případě vyberete dimenze na **Distribuce organizace**). V poli **Vlastník** na stránce **Hodnoty finančních dimenzí** můžete vybrat pracovníka pro každou finanční dimenzi.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Příklad 1: Kontroloři výdajů na základě distribucí organizace

Pracujete pro společnost Contoso Appliances a vaše organizace má šest oddělení a 10 nákladových středisek. Při odeslání nové nákupní žádanky musí nejprve přijít souhlas od vedoucího oddělení a poté od manažera nákladového střediska.

V tomto příkladu můžete nakonfigurovat dva *kontrolory výdajů na nákupní žádanky*:

- U prvního recenzenta pojmenujete oddělení a poté vyberete finanční dimenzi **Oddělení** na kartě **Distribuce organizace**. 
- U druhého recenzenta pojmenujete nákladové středisko a poté vyberete finanční dimenzi **Nákladové středisko** na kartě **Distribuce organizace**.

Při konfiguraci pracovního postupu vytvoříte dva kroky schválení. První je pro oddělení a druhý pro nákladové středisko. Pro každý schvalovací prvek vyberete **Účastník** v poli **Typ přiřazení** na kartě **Na základě rolí**, vyberte **Účastníci výdajů** v poli **Typ účastníka** a poté vyberte příslušného účastníka v poli **Účastník**.

Když je vytvořena nákupní žádanka, jsou řádkům nákupní žádanky přiřazeny finanční dimenze oddělení a nákladového střediska. Když je pracovní postup odeslán, systém nejprve vyhodnotí oddělení na nákupní žádance a přiřadí prvek schválení uživateli, který souvisí s pracovníkem, kterého jste vybrali pro oddělení. Po dokončení prvního kroku schválení systém vyhodnotí druhý krok schválení a přiřadí druhý prvek schválení uživateli, který souvisí s pracovníkem, kterého jste vybrali pro nákladové středisko.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Příklad 2: Kontroloři výdajů na základě distribucí projektu

Pracujete pro divizi služeb společnosti Contoso Appliances. Organizace vyžaduje, aby projektový manažer pro každou nákupní objednávku musel schválit výdaje. Kromě toho to musí schválit manažer nákladového střediska projektu. Schvalování lze provádět současně. V každém případě musí oba uživatelé před pokračováním pracovního postupu schválit nákupní objednávku.

V tomto příkladu vytvoříte jednoho *recenzenta výdajů nákupní objednávky*, který se jmenuje **PM a nákladové středisko**. Zaškrtnete políčko **Projektový manažer** a nastavíte možnost **Dimenze nákladového střediska** na **Ano** na kartě **Distribuce projektu** stránky **Recenzent výdajů nákupní objednávky**. Jako součást konfigurace musíte zajistit, aby pole **Projektový manažer** bylo nastaveno pro všechny projekty a pro všechny nákladová střediska na serveru byl zadán vlastník na stránce **Hodnoty finanční dimenze**.

Při konfiguraci pracovního postupu potřebujete jeden prvek schválení. Vyberete **Účastník** v poli **Typ přiřazení**. Pak na kartě **Na základě rolí** vyberete **Účastníci výdajů** v poli **Typ účastníka** a vyberete projektového manažera a nákladové středisko v poli **Účastník**. Chcete-li zajistit, aby pracovní postup nemohl pokračovat, dokud projektový manažer i vlastník nákladového střediska pracovní tok neschválí, nastavíte pole **Zásady dokončení** na **Všichni schvalovatelé**.

Když je vytvořena nákupní objednávka, pole **Projekt** musí být zadáno. Pokud nepožadujete projekt pro všechny své nákupní objednávky, měli byste do pracovního postupu přidat podmíněné rozhodnutí o kontrole projektu před spuštěním kroku schválení. Systém poté vyhodnotí projekt, který je zadán pro nákupní objednávku, a přiřadí schvalovací prvek uživateli, který je ve vztahu k pracovníkovi v poli **Projektový manažer**. Systém navíc vytvoří úkol a přiřadí ho uživateli, který souvisí s pracovníkem, kterého vyberete v poli **Majitel** pro nákladové středisko z projektu. Tento příklad používá nákladové středisko projektu, nikoli nákladové středisko nákupní objednávky.

## <a name="set-up-expenditure-reviewers"></a>Nastavení recenzentů výdajů

V tomto příkladu můžete nakonfigurovat kontrolora výdajů nákupní žádanky. Chcete-li konfigurovat další typy kontrolorů výdajů, nahraďte navigační cestu v kroku 1 příslušnou cestou z tabulky v části [Druhy kontrolorů výdajů](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) dříve v tomto tématu.

1. Přejděte na **Zásobování a získávání zdrojů \> Nastavení \> Zásady \> Recenzenti výdajů nákupních žádanek**.
2. Na stránce **Recenzenti výdajů nákupní žádanky** vyberte **Nový**.
3. Do pole **Název** zadejte název konfigurace recenzenta výdajů, například **nákladové středisko**.
4. Na pevné záložce **Kontroloři výdajů podle právnické osoby** vyberte právnickou osobu ke konfiguraci.
5. U distribuce projektu zaškrtněte políčko u každé autority projektu a vyberte **Ano** pro každou finanční dimenzi, kterou chcete povolit. 
6. Pro distribuci organizace na kartě **Distribuce organizace** vyberte **Ano** pro každou finanční dimenzi, kterou chcete povolit.
7. Opakujte kroky 4 až 6 pro každou další právnickou osobu.

## <a name="assign-owners-to-financial-dimensions"></a>Přiřazení vlastníků k finančním dimenzím

Pokud chcete k finanční dimenzi přiřadit vlastníka, postupujte takto.

1. Přejděte do části **Hlavní kniha \> Účtová osnova \> Dimenze \> Finanční dimenze**.
2. V seznamu vyberte finanční dimenzi, ke které chcete přiřadit vlastníky.
3. Vyberte **Hodnoty dimenze**.
4. Vyberte **Upravit** k provedení změn hodnot dimenze.
5. V seznamu vyberte hodnotu dimenze, ke které chcete přiřadit vlastníka.
6. V poli **Vlastník** vyberte pracovníka, kterému chcete hodnotu dimenze přiřadit.

## <a name="configure-project-distributions"></a>Konfigurace distribucí projektu

Chcete-li přiřadit autority projektu k projektu, postupujte následujícím způsobem.

1. Přejděte na **Řízení projektu a účetnictví \> Projekty \> Všechny projekty**.
2. Vyberte projekt, kterému chcete přiřadit autority.
3. Vyberte **Upravit** k provedení změn projektu.
4. Na pevné záložce **Všeobecné** v části **Odpovědný** vyberte pracovníka v polích **Manažer prodeje**, **Projektový manažer** a **Kontrolor projektu** podle potřeby.
5. Na pevné záložce **Finanční dimenze** vyberte požadované finanční dimenze pro váš projekt.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Přiřazení recenzentů výdajů k úkolu pracovního postupu

Tento příklad ukazuje, jak nakonfigurovat pracovní postup nákupní žádanky tak, aby používal kontrolora výdajů nákupní žádanky. Chcete-li konfigurovat další typy pracovních toků, stránka pracovního postupu, kterou musíte otevřít v kroku 1, může být v modulu **Správa výdajů** nebo **Závazky** namísto modulu **Zásobování a získávání zdrojů**.

Chcete-li kontrolory výdajů nákupní žádanky přidělit k úkolům pracovního postupu, postupujte následovně.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Workflow modulu Zásobování a zdroje**.
2. Dvakrát klepněte (nebo dvakrát klikněte) na existující pracovní postup nebo vytvořte nový pracovní postup.
3. V editoru pracovních postupů v podokně **Pracovní postup** vyberte úkol, ke kterému chcete přiřadit konfiguraci recenzenta výdajů. Poté v části **Podokno akcí**, ve skupině **Zobrazit** vyberte **Vlastnosti**.
4. V levém podokně stránky **Vlastnosti** vyberte **Přiřazení**.
5. Na kartě **Typ přiřazení** vyberte **Účastník**.
6. Na kartě **Na základě rolí** v poli **Typ účastníka** vyberte **Účastníci výdajů**. Poté v poli **Účastník** vyberte konfiguraci recenzenta výdajů, kterou chcete použít pro úkol pracovního postupu.
