---
title: Vytvoření vlastních polí a práce s nimi
description: Toto téma popisuje, jak v uživatelském rozhraní vytvářet vlastní pole pro přizpůsobení aplikace vašemu podnikání.
author: jasongre
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b15b25ac172e8ab942e950c9e8c4aff1e26c9291
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193848"
---
# <a name="create-and-work-with-custom-fields"></a>Vytvoření vlastních polí a práce s nimi

[!include [banner](../includes/banner.md)]

Aplikace sice poskytuje rozsáhlou škálu standardních polí pro správu širokého rozsahu obchodních procesů. Někdy však společnost potřebuje sledovat ve svém systému i další informace. Zatímco programátoři mohou tato pole přidat jako rozšíření ve vývojářských nástrojích, funkce vlastních polí umožňuje přidávat pole přímo z uživatelského rozhraní, což vám umožní přizpůsobit aplikaci tak, aby vyhovovala vašemu podniku pomocí webového prohlížeče.

*K této funkci mají přístup pouze uživatelé se zvláštními oprávněními.*

Toto video ukazuje, jak je snadné přidat na stránku vlastní pole: [Přidávání vlastních polí](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Vytváření vlastních polí

Poté, co jste identifikovali doplňující informace, které chcete v aplikaci sledovat, můžete vytvořit vlastní pole v příslušné tabulce a vystavit toto nové pole na stránce.

Proces vytváření vlastního pole a umístění daného pole ve formuláři je popsán v následujících krocích.

1. Přejděte na formulář, ve kterém chcete mít nové pole.
2. Vzhledem k tomu, že cílem je mít vlastní pole ve formuláři, vstupní bod pro vytváření vlastního pole existuje v rámci infividuálního nastavení. Otevřete panel nástrojů individuálního nastavení výběrem položky **Možnosti** a pak **Přizpůsobit tento formulář**.
3. Klikněte na **Vložit** a pak **Pole**.
4. Vyberte oblast formuláře, ve kterém chcete zveřejnit nové pole. Po výběru možnosti **Vložit pole** zobrazí dialogové okno seznam existujících polí, která lze vložit do vybrané oblasti formuláře.
5. Ověřte, že pole, které vás zajímá, již v seznamu neexistuje. Pokud ano, můžete jednoduše toto pole vybrat v seznamu a kliknout na **Vložit**.
6. Klikněte na tlačítko **Vytvořit nové pole** nad seznamem a zahájíte proces vytváření vlastního pole. Otevře se dialogové okno **Vytvořit nové pole**.

    Pokud se nezobrazí tlačítko **Vytvořit nové pole**, nemáte potřebná oprávnění k použití této funkce.

7. V dialogovém okně **Vytvořit nové pole** zadejte následující informace.
   
    1. Vyberte databázovou tabulku, do které chcete přidat toto pole. Všimněte si, že v rozevíracím seznamu se zobrazí pouze tabulky, které podporují vlastní pole. Technické podrobnosti týkající se podporovaných tabulek jsou uvedený v následující části.

    2. Zvolte zyp dat pro nové pole. Dostupné datové typy jsou zaškrtávací políčko, datum, datum a čas, desetinné číslo, číslo, rozevírací seznam a text.

        - Pokud vyberet datový typ text, můžete také určit maximální délka textu, který lze zadat do tohoto pole.
        - Pokud zvolíte typ dat rozevírací seznam, můžete také vybrat sadu platných hodnot pro toto pole.

    3. Zadejte název, popisek a text nápovědy pro dané pole. Název odpovídá názvu fyzickému názvu pole v databázi, zatímco popisek a text nápovědy jsou texty představující toto pole v uživatelském rozhraní.

8. Pokud se jedná o jediné pole, které chcete vytvořit pro tento formulář, klikněte na možnost **Uložit**. Pokud chcete vytvořit další pole, klikněte na tlačítko **Uložit a nový** a pokračujte opět krokem 7. Pamatujte, že v současnosti existuje limit **20 vlastních polí pro tabulku**.
9. Opuštěním dialogového okna **Vytvořit nové pole** se vrátíte do dialogového okna **Vložit pole**. Všechna právě přidaná vlastní pole budou automaticky označena v seznamu polí, která budou vložena do formuláře.
10. Klikněte na tlačítko **Vložit** a vložíte označená pole do vybrané oblasti formuláře.
11. **Volitelné:** Povolte režim **Přesunout** z panelu nástrojů individuálního nastavení a přesuňte nová pole na požadované místo ve vybrané oblasti. Další informace o použití různých funkcí individuálního nastavení za účelem optimalizace formuláře pro vaše osobní použití naleznete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).

> [!WARNING]
> Možnost zadávat hodnoty do vlastního pole přidaného na stránku závisí na tom, zda je tabulka přidružená k vlastnímu poli upravitelná nebo pouze pro čtení. Když je přidružená tabulka pouze pro čtení, všechna pole spojená s touto tabulkou, včetně jakýchkoli vlastních polí, budou také pouze pro čtení.


## <a name="sharing-custom-fields-with-other-users"></a>Sdílení vlastních polí s dalšími uživateli

Po vytvoření vlastního pole a jeho vystavení na stránce můžete chtít poskytnout toto aktualizované zobrazení stránky s novým polem jiným uživatelům v systému. Toho lze dosáhnout dvěma různými způsoby pomocí možností individuálního nastavení produktu:

- Doporučená cesta je **publikovat [uložené zobrazení](saved-views.md)** s vlastním polem přidaným na stránku k příslušné sadě uživatelů. Pokud není funkce uložených pohledů povolena, může správce systému použít personalizaci na požadované uživatele z přizpůsobovacího formuláře. Další informace najdete v části [Přizpůsobení uživatelského prostředí](personalize-user-experience.md).
- Případně můžete exportovat své změny (nazývané *individuální nastavení*), zaslat je jednomu nebo více uživatelům a nechat tyto jednotlivé uživatelé importovat vaše změny. Možnost **Spravovat** na panelu nástrojů induviduálního nastavení vám umožní exportovat a importovat individuální nastavení.

## <a name="managing-custom-fields"></a>Správa vlastních polí

Správu všech vlastních polí v systému lze provádět pomocí stránky **Vlastní pole** v modulu Správa systému. Tato stránku umožňuje uživatelům přístup k mnoha možnostem, včetně:

- Zobrazení seznamu všech vlastních polí v systému.
- Omezené úpravy existujících vlastních polí.
- Odstranění vlastních polí.
- Vystavení vlastních polí na datových entitách.
- Poskytnutí překladů popisků vlastních polí a textu nápovědy.

### <a name="viewing-all-custom-fields"></a>Zobrazení všech vlastních polí

Stránka **Vlastní pole** poskytuje zobrazení všech vlastních polí, která bylá definována v systému. Jednoduše vyberte tabulku, která vás zajímá, a stránka se zaktualizuje a zobrazí seznam vlastních polí přidružených k tabulce. Výběr vlastního pole ze seznamu vám umožní zobrazit všechny podrobnosti o poli.

### <a name="editing-custom-fields"></a>Úprava vlastních polí

Po vytvoření vlastního pole lze upravit pouze určité části informací o vlastních polích na stránce **Vlastní pole**.

*Můžete* změnit tyto atributy:

- Popisek
- Text nápovědy
- Délka textových polí

*Nemůžete* upravit následující atributy:

- Název pole
- Datový typ

Pro rozevírací seznam polí lze také změnit uspořádání sady platných hodnot pro vlastní pole a přidat nové hodnoty. Nicméně existující hodnoty rozevíracího seznamu polí nelze odebrat. Nezapomeňte kliknout na **Použít změny** po dokončení úprav polí pro určitou tabulku, aby se změny uložily.

### <a name="exposing-custom-fields-on-data-entities"></a>Vystavení vlastních polí na datových entitách

Je rovněž důležité umožnit, aby byla vlastní pole viditelná na datových entitách. Datové entity se používají ve funkci [Přehled integrace Office](../../dev-itpro/office-integration/office-integration.md), stejně jako u scénáře importu a exportu dat.

Pro vystavení vlastního pole na datové entitě postupujte podle těchto kroků:

1. Vyberte vlastní pole ve formuláři **Vlastní pole**.
2. Rozbalte část **Entity** a zobrazte sadu příslušných entit.
3. Klikněte na tlačítko **Upravit**.
4. Změňte pole **Povoleno**, které má být vybráno pro každou entitu, která vystaví toto pole.
5. Kliknutím na tlačítko **Použít změny** uložte své volby.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Povolení zobrazení vlastních polí v jiných jazycích

Vzhledem k tomu, že vlastní pole mohou být vyžadována v různých jazycích, poskytuje stránka **Vlastní pole** mechanismus, který umožní překlad popisku a textu nápovědy vlastního pole do dalších jazyků.

Následující kroky popisují proces překladu vlastních polí do jiných jazyků:

1. Vyberte vlastní pole na stránce **Vlastní pole**.
2. Výběr tlačítko **Překlady** v podokně akcí. Otevře se rozevírací nabídka s existujícími překlady pro toto pole.
3. Rozevírací nabídka **Jazyk** zobrazuje sadu jazyků, pro které již byly poskytnuty překlady.

    Pokud chcete upravit stávající překlad, z nabídky vyberte požadovaný jazyk a upravte hodnoty pro popisek a text nápovědy.

    V opačném případě klikněte natlačítko **Přidat jazyk**, vyberte požadovaný jazyk z nabídky a potom zadejte přeložené hodnoty pro popisek a text nápovědy.

4. Po dokončení klikněte na tlačítko **OK**.

### <a name="deleting-custom-fields"></a>Odstranění vlastních polí

Ve výjimečných případech se můžete rozhodnout, že vlastní pole již není potřeba. V takovém případě může správce systému odstranit pole ze stránky **Vlastní pole**. Je třeba vybrat správné pole, kliknout na **Odstranit**, kliknout na **Ano** pro potvrzení odstranění a nakonec kliknout na tlačítko **Použít změny**.

> [!NOTE]
> Tuto akci nelze vrátit zpět a výsledkem bude, že data spojená s polem budou natrvalo odstraněna z databáze.

## <a name="appendix"></a>Dodatek

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Proč nemohu zadat hodnotu do svého vlastního pole? 

Pokud nemůžete zadat hodnotu do vlastního pole, když je stránka v režimu úprav, může to být proto, že tabulka, do které bylo pole přidáno, je aktuálně pouze pro čtení. Všechna pole v tabulce se stanou pouze pro čtení, pokud je záložní tabulka aktuálně nakonfigurována jako jen pro čtení na stránce.   

### <a name="who-can-create-custom-fields"></a>Kdo může vytvářet vlastní pole?

Jako ochranné opatření je ve výchozím nastavení umožněno vytváření vlastních polí pouze správcům systému. Nicméně uživatelům typu power user, které určí organizace, mohou být přidělena práva k vytváření vlastních polí od správce systému pomocí role zabezpečení **Uživatel power user přizpůsobení runtime**. Uživatelé bez této role zabezpečení nebudete moci vytvářet vlastní pole, ale stále budou moci zobrazit nebo používat vlastní pole přidaná ostatními uživateli v systému.

### <a name="what-tables-support-custom-fields"></a>Jaké tabulky podporují vlastní pole?

Z důvodů výkonnosti a z technických důvodů momentálně podporují přidání vlastních polí pouze tabulky splňující následující podmínky.

- Tabulka musí být označena jako jedna z těchto skupin:

    - Seskupit
    - WorksheetHeader
    - Hlavní
    - Různé
    - Parametr
    - Odkaz
    - TransactionHeader

- Tabulka nemůže rozšiřovat jinou tabulku.
- Tabulka nemůže být označena jako systémová tabulka.
- Tabulka nemůže být dočasná.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Lze odkazovat na vlastní pole z nástrojů pro vývojáře?  

Vlastní pole lze spravovat pouze prostřednictvím uživatelského rozhraní a nelze na ně odkazovat pomocí kódu. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
