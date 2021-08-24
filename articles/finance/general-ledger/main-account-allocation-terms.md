---
title: Podmínky přidělení
description: Toto téma obsahuje informace o používání podmínek přidělování na hlavním účtu.
author: rachel-profitt
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 957baba1364fbbd4a51c6f51b0fad5bf8db46680fa97b9d3d0474dc015064609
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776521"
---
# <a name="allocation-terms"></a>Podmínky přidělení

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o používání podmínek přidělování na hlavním účtu. Podmínky přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo výnosy účtovaly v účetnictví na správný objekt.

Každá podmínka alokace, kterou vytvoříte na hlavním účtu, definuje procento voucheru, který má být přidělen z jediného zdroje, a kombinace finančních dimenzí. Kromě toho definujete hlavní cílový účet a finanční dimenze, kam bude částka přidělena. 

Při definování finanční dimenze zdroje pro alokaci můžete vybrat, zda je každá dimenze specifická nebo nespecifická. Konkrétní označuje, že finanční dimenze pro zdrojovou transakci musí odpovídat vybrané dimenzi. Pokud vyberete nespecifické, znamená to, že ke shodě může přispět jakákoli hodnota pro finanční dimenzi.

Při definování cílového účtu účetní knihy pro alokační období musíte zadat hlavní účet, ke kterému přidělujete částku. Můžete použít stejný hlavní účet, na který je zdrojová transakce zaúčtována, nebo jiný hlavní účet. Pokud je použit stejný hlavní účet, zobrazí se při ukládání záznamu varování. Kromě určení hlavního účtu musíte také zadat cílové dimenze. Pro každou dimenzi můžete určit, zda chcete zachovat hodnotu finanční dimenze zdroje nebo ji změnit. Pokud vyberete ne, musíte pro finanční dimenzi vybrat novou hodnotu. Pokud vyberete Ano, nebudou zadány žádné další informace a systém při zveřejnění zachová původní finanční dimenzi.

Počet podmínek přidělování, které můžete přidat na hlavní účet, není nijak omezen; součet procent přidělených na alokační období však nesmí přesáhnout 100. Pokud by část původní částky voucheru měla zůstat ve zdrojových finančních dimenzích, můžete vytvořit přidělení za méně než 100 procent. Podmínky přidělení mohou být přidány na hlavní účet jako přepsání právnické osoby. Pokud používáte sdílenou účtovou osnovu, musí být pro každou právnickou osobu definovány podmínky přidělování. Pro přístup k tlačítku **Podmínky přidělení** musíte nejprve zaškrtnout políčko **Přidělení** v okně Přepis právnické osoby.

## <a name="allocation-term-example"></a>Příklad podmínek přidělení
Pro svou organizaci jste definovali nákladové středisko s názvem CORPORATE, které má číslo 000. Když jsou zaúčtovány faktury za náklady na služby, jsou kódovány do tohoto PODNIKOVÉHO nákladového střediska. Vaše společnost definovala pravidlo, že všechny náklady na služby by měly být přiděleny podle procenta každému z jednotlivých nákladových středisek. Ostatní finanční dimenze oddělení a obchodní jednotky zůstanou stejné.

V tomto příkladu by se pro hlavní účet nákladů na veřejné služby vytvořil nový alokační termín. Pro každé nákladové středisko by byl vytvořen jeden řádek s procentem, který má být přidělen. **Kritéria výběru** pro finanční dimenze zdroje pro každý řádek by byla **specifický** pro **Nákladové středisko** a hodnota by byla nastavena na 000: CORPORATE. Pro oddělení a obchodní jednotku by **Kritéria výběru** byla **Nespecifické**.

Na pevné záložce **Cílový účet hlavní knihy** bude hlavní účet stejný výdajový účet služeb a hodnota **Zachovat zdrojové finanční dimenze** bude nastavena na **ano** pro **Obchodní jednotku** a **Oddělení.** Volba **Udržovat finanční dimenze zdroje** bude nastavena na **Ne** pro **Nákladové středisko** a vybraná hodnota bude každé příslušné nákladové středisko, které přidělujete. Pokud existují tři nákladová střediska pro přidělení, vytvořily by se tři záznamy o podmínkách přidělování. Jediným rozdílem mezi jednotlivými podmínkami alokace je nákladové středisko, které je uvedeno na účtu cílové knihy.

## <a name="create-an-allocation-term-on-a-main-account"></a>Vytvoření podmínky alokace na hlavním účtu

1. V **navigačním podokně** přejděte na > **Moduly >Hlavní kniha > Účtová osnova > Účty > Hlavní účty**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Na pevné záložce **Přepisy právnické osoby** vyberte **Přidat**.
4. Vyberte **Společnost** a pak vyberte **Přidat**.
5. Zaškrtněte políčko **Přidělení**.
6. Vyberte **Podmínky přidělení**.
7. Vyberte **Upravit** pro úpravu výchozího záznamu nebo **Nový** pro přidání záznamu.
8. V poli **Procento** zadejte procento transakcí voucherů, které chcete alokovat.
9. Na pevné záložce **Zdrojová finanční dimenze** v okně **Kritéria výběru** vyberte možnost pro každou finanční dimenzi.
    - Pokud vyberete **Specifický**, pak v rozevíracím seznamu napravo vyberte hodnotu finanční dimenze.
    - Pokud vyberete **Nespecifické**, pro finanční dimenzi nejsou vyžadovány žádné další informace.
10. Na pevné záložce účtu **Cílová hlavní kniha** v poli **Na účet** vyberte hlavní účet, na který chcete alokovat procentuální podíl na transakci voucheru.
11. V poli **Udržovat finanční dimenze zdroje** vyberte možnost pro každou finanční dimenzi.
    - Pokud vyberete **Ne**, pak v rozevíracím seznamu napravo, kam má být transakce voucheru přiřazena, vyberte hodnotu finanční dimenze.
    - Pokud vyberete **Ano**, nejsou vyžadovány žádné další informace. Při zveřejnění přidělení si systém ponechá hodnotu na původním voucheru.
12. Opakujte kroky 7 až 11 pro každé další přidělení. Součet všech přidělení je uveden v poli **Celkem procent**. Tato částka nesmí přesáhnout 100.
13. Zavřete všechny stránky.

>[!NOTE] 
> Můžete volitelně použít tlačítko **Kopírovat** pro duplikování vybrané alokace.

Když je pro hlavní účet vytvořen termín přidělení, systém automaticky zaúčtuje nový voucher, když je zaúčtován voucher, který odpovídá zdrojovým finančním dimenzím v podmínkách přidělení.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]