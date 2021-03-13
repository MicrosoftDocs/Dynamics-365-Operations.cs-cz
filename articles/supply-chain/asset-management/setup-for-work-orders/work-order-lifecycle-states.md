---
title: Stavy životního cyklu pracovního příkazu
description: Toto téma vysvětluje stavy životního cyklu pracovního příkazu v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2a8052942ff97c9e8033d5915723e82c42f964c8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021572"
---
# <a name="work-order-lifecycle-states"></a>Stavy životního cyklu pracovního příkazu


[!include [banner](../../includes/banner.md)]

 

Stavy životního cyklu pracovního příkazu určují stavy, kterými může pracovní příkaz projít. Příkladem může být **Vytvořeno**, **Naplánováno**, **Probíhá** a **Ukončeno**. Stavy životního cyklu pracovního příkazu lze aktualizovat ručně v rámci pracovního příkazu nebo je lze aktualizovat automaticky (například během plánování pracovních příkazů).

Stavy životního cyklu pracovního příkazu, které jsou vyžadovány pro vaše pracovní příkazy, musí být připojeny k fázím odpovídajícího projektu na stránce **Parametry modulu Řízení a účetnictví projektu** (**Řízení projektů a účetnictví** \> **Parametry modulu Řízení a účetnictví projektu**). Nejprve nastavíte fáze projektu v modulu řízení a účetnictví projektu. Poté nastavíte stavy životního cyklu pracovních příkazů a modely životního cyklu pracovních příkazů ve správě majetku.

V následující tabulce jsou popsány možnosti v oddílech **Pracovní příkaz** a **Plánovat** na pevné záložce **Obecné** na stránce **Stav životního cyklu pracovního příkazu** (**Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Stavy životního cyklu**).

![Stav životního cyklu pracovního příkazu](media/09-setup-for-work-orders.png)

| Název možnosti                   | Popis |
|-------------------------------|-------------|
| Aktivní                        | Tuto možnost nastavte na **Ano**, má-li být pracovní příkaz aktivní v tomto stavu životního cyklu. |
| Přidat řádek                      | Nastavte tuto možnost na **Ano**, chcete-li do pracovního příkazu, který je v tomto stavu životního cyklu, přidat úlohy pracovního příkazu |
| Odstranit                        | Tuto možnost nastavte na **Ano**, může-li být pracovní příkaz odstraněn v tomto stavu životního cyklu. |
| Odstranit řádek                   | Nastavte tuto možnost na **Ano**, lze-li odebrat úlohy pracovního příkazu z pracovního příkazu, který je v tomto stavu životního cyklu. |
| Povolit plánování              | Tuto možnost nastavte na **Ano**, může-li být pracovní příkaz naplánován v tomto stavu životního cyklu. |
| Zadat skutečný začátek              | Tuto možnost nastavte na **Ano** v případě, že má být uživatel vyzván k výběru skutečného počátečního data a času pro pracovní příkaz, když je aktualizován v tomto stavu životního cyklu. |
| Zadat skutečný konec                | Tuto možnost nastavte na **Ano** v případě, že má být uživatel vyzván k výběru skutečného koncového data a času pro pracovní příkaz, když je aktualizován v tomto stavu životního cyklu. |
| Zaúčtovat deníky                 | Nastavte tuto možnost na **Ano**, chcete-li, aby byl deník pracovního příkazu automaticky zaúčtován při aktualizaci pracovního příkazu do tohoto životního cyklu. Pokud při účtování deníku dojde k chybě, zobrazí se zpráva a aktualizace stavu životního cyklu pracovního příkazu je zrušena. Chcete-li zobrazit řádky deníku pro pracovní příkaz, vyberte **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy**, **Aktivní pracovní příkazy** nebo **Moje aktivní pracovní příkazy**, vyberte pracovní příkaz ze seznamu a vyberte **Deníky**. Toto nastavení automatického zaúčtování deníku pracovních příkazů v určitém stavu životního cyklu je stejné jako při výběru možnosti **Zaúčtovat deníky** na stránce **Deníky pracovních příkazů**.<p>**Poznámka:** nastavíte-li tuto možnost na **Ano**, deníky budou automaticky zaúčtovány v případě, že nebyl nastaven žádný Workflow schválení. Pokud vaše společnost používá nastavení schválení deníku, které je nakonfigurováno na stránce **Schválení deníku** (**Řízení projektů a účetnictví** \> **Nastavení** \> **Deníky** \> **Schválení deníku**), manažer nebo úředník musí ověřit a zaúčtovat registrace spotřeby.</p> |
| Zpracovat kontrolní seznam údržby | Nastavte tuto možnost na **Ano**, chcete-li, aby byly zpracovány všechny kontrolní seznamy údržby při aktualizaci pracovního příkazu do tohoto životního cyklu. V rámci zpracování jsou zaúčtovány všechny registrace čítačů provedené v kontrolním seznamu údržby a je vyhodnocen výsledek celého kontrolního seznamu údržby. Řádky kontrolního seznamu údržby s výsledkem **Úspěšný** a **Chyba** jsou vyhodnoceny a pokud nejméně jeden řádek selže, je celý kontrolní seznam údržby označen jako **Neúspěšný** ve správě majetku. |
| Připraven                         | Tuto možnost nastavte na **Ano**, pokud se stav plánu úlohy pracovního příkazu pro všechny úlohy pracovního příkazu, které jsou vytvořeny na pracovním příkazu, musí být automaticky aktualizován na **Připraven** při aktualizaci pracovní objednávky do tohoto stavu životního cyklu. |
| Začátek                         | Tuto možnost nastavte na **Ano**, pokud se stav plánu úlohy pracovního příkazu pro všechny úlohy pracovního příkazu, které jsou vytvořeny na pracovním příkazu, musí být automaticky aktualizován na **Zahájeno** při aktualizaci pracovní objednávky do tohoto stavu životního cyklu. |
| Konec                           | Tuto možnost nastavte na **Ano**, pokud se stav plánu úlohy pracovního příkazu pro všechny úlohy pracovního příkazu, které jsou vytvořeny na pracovním příkazu, musí být automaticky aktualizován na **Ukončeno** při aktualizaci pracovní objednávky do tohoto stavu životního cyklu. |
| Odstranit řádky plánování         | Tuto možnost nastavte na **Ano**, pokud plánování všech úloh pracovního příkazu vytvořených na pracovním příkazu, které jsou již naplánovány, by měly být odstraněny při aktualizaci pracovní objednávky do tohoto stavu životního cyklu. Jinými slovy, rezervace kapacity majetku, související pracovník údržby a související nástroje budou odstraněny. Můžete například nastavit tuto možnost na **Ano** ve stavu životního cyklu pracovního příkazu s názvem **Odhadnuto**. Poté, co je do tohoto stavu životního cyklu vrácen pracovní příkaz, protože je vyžadováno přeplánování, lze z tohoto pracovního příkazu odstranit plánování. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Nastavit fáze projektu a stavy životního cyklu pracovních příkazů

1. Vyberte **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.
2. Na kartě **Fáze projektu** pro každou fázi, kterou chcete použít, zaškrtněte políčko pro každý typ projektu vyžadovaný pro vaše pracovní příkazy. Typy projektu definují pravidla o povolených finančních úkolech. Příklady finančních úkolů jsou vytvoření prognózy, vytvoření odhadů a vytvoření počátečních zůstatků.

    > [!IMPORTANT]
    > Není-li pro typ projektu vybrána fáze projektu, ale fáze projektu je použita pro stav životního cyklu pracovního příkazu, projekty pracovního příkazu nebudou odpovídajícím způsobem aktualizovány.

3. Zavřete stránku **Parametry modulu Řízení a účetnictví projektu**.
4. Vyberte **Správa majetku**\>**Nastavení**\> **Pracovní příkazy** \>**Stavy životního cyklu**.
5. Zvolte **Nový** pro vytvoření stavu životního cyklu pracovního příkazu.
6. Do pole **Stav životního cyklu** zadejte ID stavu životního cyklu.
7. Do pole **Název** zadejte název.

    Na pevné záložce **Podrobnosti** pole **Modely životního cyklu** zobrazuje počet modelů životního cyklu pracovního příkazu, které používají tento stav životního cyklu.

8. Na pevné záložce **Obecné** v oddíle **Pracovní příkaz** vyberte funkce, které mají být k dispozici pro tento stav životního cyklu, nastavením příslušných možností na **Ano**. Jednotlivé možnosti jsou popsány ve výše uvedené tabulce v tomto tématu.
9. V části **Projekt** vyberte v poli **Fáze** fázi projektu, která má být spojena s tímto stavem životního cyklu.
10. V oddílu **Projekt** nastavte možnost **uzavřít aktivity** na **Ano**, chcete-li, aby byly aktivity projektu související s každou úlohou pracovního příkazu byly automaticky uzavřeny v tomto stavu životního cyklu.

    > [!NOTE]
    > Chcete-li najít číslo aktivity projektu, která souvisí s úlohou pracovního příkazu, vyberte **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy**, **Aktivní pracovní příkazy** nebo **Moje aktivní pracovní příkazy**. Otevřete pracovní přkazu a poté vyberte úlohu pracovního příkazu. Číslo aktivity je zobrazeno v poli **Číslo aktivity** v oddílu **Projekt** na kartě **Obecné** na pevné záložce **Podrobnosti řádku**.

11. V oddílu **Prognóza** nastavte možnost **Kopírovat prognózu hodin**, **Kopírovat prognózu položek** a/nebo **Kopírovat prognózu výdajů** na **Ano**, pokud mají být prognózy projektu pracovního příkazu automaticky zkopírovány do deníků pracovních příkazů, pokud je tento pracovní příkaz v tomto stavu životního cyklu.
12. V části **Plán** nastavte jednu z možností na **Ano**, pokud má být stav plánu pro úlohy pracovních příkazů aktualizován, když je pracovní příkaz v tomto stavu životního cyklu. Popisy možností pro možnosti **Dokončení**, **Zahájení**, **Ukončení** a **Odstranění řádků** plánu naleznete v tabulce dříve v tomto tématu.

    > [!NOTE]
    > Chcete-li zobrazit řádky plánu, které souvisí s úlohami pracovního příkazu, vyberte **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy**, **Aktivní pracovní příkazy** nebo **Moje aktivní pracovní příkazy**. Otevřete pracovní příkaz, vyberte úlohu pracovního příkazu na pevné záložce **Úlohy pracovního příkazu** a zobrazte související informace na záložce s náhledem **Podrobnosti řádku**. V poli **Stav** na kartě **Plán** se zobrazuje stav úlohy pracovního příkazu. Pole **Stav** může být nastaveno na následující hodnoty: **Naplánováno**, **Připraveno**, **Zahájeno**, **Zastaveno** a **Ukončeno**.

13. V části **Požadavky na údržbu** vyberte v poli **Stav životního cyklu** stav životního cyklu požadavku na údržbu, na který mají být aktualizovány související požadavky na údržbu. Tato aktualizace se automaticky spustí. Lze ji provést pouze v případě, že je v modelu životního cyklu požadavku na údržbu, který se používá pro požadavek na údržbu, vybrána možnost stav životního cyklu žádosti o údržbu.
14. V části **Majetek** nastavte volbu **Aktualizovat kusovník majetku** na **Ano**, pokud se mají při aktualizaci pracovního příkazu automaticky aktualizovat všechny položky použité na pracovním příkazu na stránce **Kusovník majetku** do tohoto stavu životního cyklu. Toto nastavení může být důležité, pokud například stav životního cyklu pracovního příkazu definuje pracovní příkaz jako dokončený nebo ukončený.
15. V části **Fond pracovních objednávek** nastavte volbu **Odstranit odkaz na fond** na **Ano**, pokud mají být z fondů pracovních příkazů automaticky odstraněny pracovní příkazy, které jsou v tomto stavu životního cyklu.
16. Na pevné záložce **Ověřit** vyberte typy ověření, které mají být aktivovány v tomto stavu životního cyklu, nastavením příslušných možností na **Ano**. Potom v poli **Typ** pro každý vybraný typ ověřování vyberte typ zprávy, která se má zobrazit, pokud nebyla ověřena povinná pole související s typem ověření. Vyberete-li možnost **Chyba**, bude aktualizace stavu životního cyklu pracovního příkazu zrušena, dokud nebudou v daném pracovním příkazu aktualizovány související povinná pole.

    - Volby **Prostoj údržby**, **Kontrolní seznam údržby**, **Příznak poruchy**, **Příčina poruchy** a **Náprava poruchy** souvisí s volbami v oddílu **Povinné** na stránce **Typ pracovních příkazů** (**Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Typy pracovních příkazů**). Chcete-li tato ověření aktivovat, musí být související možnosti nastaveny také na **Ano** u typu pracovního příkazu, který se používá pro daný pracovní příkaz.
    - Je-li možnost **Kontrolní seznam údržby** nastavena na **Ano** pro stav životního cyklu, na který je aktualizován pracovní příkaz, ověření je provedeno za účelem ověření, že řádky kontrolního seznamu údržby označené jako **Povinné** mají byla registrovány jako **Kontrolované** nebo **Nepoužívané**. Pokud nebyly v povinných řádcích provedeny žádné z těchto registrací, zobrazí se při aktualizaci pracovního příkazu na tento stav životního cyklu informační, chybové či varovné zprávy.
    - Je-li možnost **Potvrzené náklady** nastavena na **Ano** pro stav životního cyklu, na který je aktualizován pracovní příkaz, bude vypočtena celková částka potvrzených nákladů (tj. celková částka výdajů potvrzených právnickou osobou k výplatě) pro každou úlohu pracovního příkazu. Pokud je částka potvrzených nákladů větší než 0 (nula), zobrazí se zpráva. Vyberte typy nákladového závazku, které jsou zahrnuty na pevné záložce **Nákladové závazky**, na kartě **Řízení nákladů** na stránce **Parametry modulu Řízení a účetnictví projektu** (**Řízení a účetnictví projektu** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**).
    - Je-li možnost **Prostoj údržby** nastavena na **Ano** pro stav životního cyklu, na který je aktualizován pracovní příkaz, bude ověření prostoje údržby provedeno u majetku souvisejícího s tímto pracovním příkazem. Pokud byla provedena registrace prostojů údržby, ale nedošlo k žádnému **Ukončení** registrace, zobrazí se při aktualizaci pracovního příkazu do tohoto stavu životního cyklu zpráva.
    - Pokud standardní nastavení projektu nezahrnuje všechny fáze, které požadujete pro nastavení správy majetku, můžete nastavit uživatelem definované fáze projektu na kartě **Fáze projektu** na stránce **Parametry modulu Řízení a účetnictví projektu**. Na následujícím obrázku je zobrazena karta **Fáze projektu** na stránce **Parametry modulu Řízení a účetnictví projektu**.

    ![Stránka Nastavit fáze projektu pro různé typy projektů](media/10-setup-for-work-orders.png)

> [!NOTE]
> Pokud stav životního cyklu, na který aktualizujete pracovní příkaz, je neaktivní, deníky související s tímto pracovním příkazem, které dosud nebyly zaúčtovány, budou automaticky odstraněny. Toto chování pomáhá zaručit automatické vyčištění nepoužívaných dat. (Stav životního cyklu je neaktivní, pokud je možnost **Aktivní** nastavena na **Ne** na pevné záložce **Obecné** na stránce **Stav životního cyklu pracovního příkazu**.)
>
> Pokud však nastavíte pracovní příkaz jako neaktivní ručně, deníky související s tímto pracovním příkazem, které dosud nebyly zaúčtovány, **nebudou** automaticky odstraněny. (Chcete-li ručně deaktivovat pracovní příkaz, vyberte možnost **Správa majetku** \> **Společné** \> **Pracovní příkazy** \> **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**. Otevřete pracovní příkaz a přepněte se do zobrazení **Záhlaví**. Na pevné záložce **Obcné** vyberte **Upravit** a nastavte možnost **Aktivní** na **Ne**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Vztahy mezi modely životního cyklu pracovních příkazů, typy pracovních příkazů a stavy životního cyklu pracovních příkazů.

Modely životního cyklu odkazují na workflowy a stavy životního cyklu jsou vybrány v modelu životního cyklu v sekvenčním pořadí. Modely životního cyklu se nastavují v typech pracovních příkazů. Typy pracovních příkazů určují velikost nebo rozsah pracovních postupů a pracovních procesů. Například **Údržba**, která je standardní typ pracovního příkazu, může souviset s modelem životního cyklu pracovních příkazů, který má mnoho stavů životního cyklu. Naopak můžete mít typ **Opravného** pracovního příkazu, který se používá pro neplánované pracovní příkazy nebo pro pracovní příkazy, v nichž je úloha dokončena před provedením pracovního příkazu z důvodu naléhavé situace. Tento typ pracovního příkazu může souviset s modelem životního cyklu pracovních příkazů, který má pouze několik stavů životního cyklu.

Důvodem pro použití typů je to, že při definování typu, například podle pracovního příkazu nebo majetku, jsou související pracovní procesy (stavy životního cyklu) definovány automaticky. Další informace o nastavení typů pracovních příkazů naleznete v tématu [Typy pracovních příkazů](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Stavy životního cyklu, modely životního cyklu a typy se používají pro funkční místa, majetek a požadavky na údržbu kromě pracovních příkazů.

Na následujícím obrázku je znázorněn vztah mezi typy pracovních příkazů, modely životního cyklu a stavy životního cyklu.

![Stránka typ pracovní objednávky ve srovnání s pracovní objednávkou – stránka Modely životního cyklu](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Modely životního cyklu pracovního příkazu

Po vytvoření stavů životního cyklu pracovního příkazu, které jsou požadovány pro vaše pracovní příkazy, je lze rozdělit do modelů životního cyklu pracovních příkazů. Měli byste alespoň vytvořit jeden standardní model životního cyklu.

1. Vyberte **Správa majetku**\>**Nastavení**\> **Pracovní příkazy** \>**Modely životního cyklu**.
2. Zvolte **Nový** pro vytvoření modelu životního cyklu pracovního příkazu.
3. Do pole **Model životního cyklu** zadejte ID modelu životního cyklu.
4. Do pole **Název** zadejte název.

    Na kartě **Podrobnosti** ukazuje pole **Stavy životního cyklu** počet stavů životního cyklu, které jsou vybrány v tomto modelu životního cyklu majetku. Pole **Typy pracovních příkazů** zobrazuje počet typů pracovních příkazů, které používají tento model životního cyklu.

5. Na kartě **Stavy životního cyklu** vyberte stavy životního cyklu, které si přejete zahrnout v modelu životního cyklu:

    - Chcete-li v modelu životního cyklu použít stav životního cyklu, vyberte jej v části **Zbývající stavy životního cyklu** a potom vyberte tlačítko šipky vpravo ![Šipka vpravo](media/12-setup-for-work-orders.png) a přesuňte jej do části **Vybrané stavy životního cyklu**.
    - Chcete-li do modelu životního cyklu zahrnout všechny dostupné stavy životního cyklu, vyberte tlačítko **Vybrat všechny dostupné fáze** ![Vybrat všechny dostupné fáze](media/13-setup-for-work-orders.png). Všechny stavy životního cyklu jsou přesunuty do části **Vybrané stavy životního cyklu**.
    - Chcete-li z modelu životního cyklu odebrat stav životního cyklu, vyberte jej v části **Vybrané stavy životního cyklu** a potom vyberte tlačítko šipky vlevo ![Šipka vlevo](media/14-setup-for-work-orders.png) a přesuňte jej do části **Zbývající stavy životního cyklu**.

6. Vyberte **Aktualizace stavu životního cyklu**, chcete-li definovat stavy životního cyklu, které mohou následovat po vybraném stavu životního cyklu.
7. Na pevné záložce **Aktualizace** v poli **Plánovaný stav** vyberte stav životního cyklu, který by měl být vždy vybrán pro pracovní příkaz, pro který jste dokončili plánování pracovních úkolů, bez ohledu na předchozí stav životního cyklu pracovního příkazu.
8. V poli **Neplánovaný stav životného cyklu** vyberte stav životního cyklu, který by měl být vybrán vždy pro pracovní příkaz v případě, že je odstraněno plánování pracovního příkazu.
9. Uložte model životního cyklu pracovních příkazů.

![Stránka Modely životního cyklu pracovního příkazu](media/15-setup-for-work-orders.png)
