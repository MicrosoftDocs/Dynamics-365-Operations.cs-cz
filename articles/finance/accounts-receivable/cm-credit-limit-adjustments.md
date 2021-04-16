---
title: Úpravy limitu úvěru
description: Toto téma vysvětluje, jak nastavit a přidat úpravy limitu úvěru.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1669029f28cef924170b47340567af49525e1b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835357"
---
# <a name="credit-limit-adjustments"></a>Úpravy limitu úvěru 

[!include [banner](../includes/banner.md)]

Úpravy limitu úvěru umožňují správcům úvěrů aktualizovat limity úvěru a data vypršení platnosti jednoho odběratele, skupiny odběratelů nebo všech odběratelů prostřednictvím procesu zaúčtování. Můžete přidávat položky úpravy limitu úvěru pro aktualizaci odběratelů a skupin odběratelů podle limitu úvěru nebo je použít k výpočtu automatických limitů úvěrů. Tyto položky pak mohou být zkontrolovány, odeslány ke schválení prostřednictvím workflow a zaúčtovány na účty odběratelů.

## <a name="set-up-credit-limit-adjustments"></a>Nastavení úprav limitu úvěru

Položky deníku úprav limitu úvěru můžete vytvořit na stránce **Úprava limitu úvěru** (**Správa úvěru \> Úpravy limitu úvěru \> Úpravy limitu úvěru**).

1. Zvolte **Nové**. Je vytvořena nová skupina položek s číslem úpravy limitu úvěru.
2. Vyberte typ úpravy limitu úvěru:

    - Výběrem možnosti **Limit úvěru** můžete změnit limit úvěru odběratele.
    - Výběrem možnosti **Dočasný limit úvěru** můžete vytvořit dočasný limit úvěru namísto změny aktuálního limitu úvěru odběratele. Dočasné limity úvěru ruší limit úvěru odběratele po stanovenou dobu. Po uplynutí tohoto období se znovu použije limit úvěru odběratele.
3. Zadejte popis. 

Je-li označeno políčko **Zaúčtováno**, limity úvěru byly použity. V poli **Stav schválení** je uveden stav workflow deníku. Workflow je volitelné.

### <a name="add-credit-limit-adjustments"></a>Přidání úprav limitu úvěru

Chcete-li ručně přidat úpravy limitu úvěru, zvolte **Řádky** a poté proveďte následující kroky.

1. Chcete-li přidat úpravu limitu úvěru pro odběratele, použijte nabídku **Úpravy odběratele**. Chcete-li přidat limit úvěru pro skupinu odběratelů podle limitu úvěru, zvolte možnost **Úpravy skupiny odběratelů podle limitu úvěru**.
2. Zadejte účet odběratele pro účet odběratele na faktuře, který je třeba aktualizovat pomocí nového limitu úvěru. Pokud jste v kroku 1 vybrali možnost **Úpravy skupiny odběratelů podle limitu úvěru**, zadejte skupinu odběratelů podle limitu úvěru. Do stejného řádku deníku nelze zadat jak účet odběratele, tak i ID skupiny odběratelů podle limitu úvěru.

    Je zobrazen aktuální limit úvěru a automaticky se zobrazí název.

3. Zadejte nový limit úvěru, který by měl při zaúčtování položky limitu úvěru nahradit aktuální limit úvěru.
4. Chcete-li definovat nové datum vypršení platnosti pro limit úvěru odběratele, zadejte datum. Při vytvoření úpravy limitu úvěru je nutné zadat datum vypršení platnosti limitu úvěru.

V poli **Stav schválení** je uveden stav workflow řádku deníku.

Chcete-li automaticky generovat úpravy limitu úvěru, můžete použít nabídku **Generovat** v podokně Akce.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Přidání úprav dočasného limitu úvěru

Chcete-li ručně přidat úpravy dočasného limitu úvěru, postupujte tímto způsobem u řádků deníku.

1. Chcete-li přidat úpravu limitu úvěru pro odběratele, použijte nabídku **Úpravy odběratele**. Chcete-li přidat limit úvěru pro skupinu odběratelů podle limitu úvěru, zvolte možnost **Úpravy skupiny odběratelů podle limitu úvěru**.
2. Zadejte účet odběratele pro účet odběratele na faktuře, který je třeba aktualizovat pomocí nového limitu úvěru. Pokud jste v kroku 1 vybrali možnost **Úpravy skupiny odběratelů podle limitu úvěru**, zadejte skupinu odběratelů podle limitu úvěru. Do stejného řádku deníku nelze zadat jak účet odběratele, tak i ID skupiny odběratelů podle limitu úvěru.

    Pokud již existuje aktivní nebo budoucí dočasný limit úvěru, zobrazí se u každého dočasného limitu úvěru aktuální dočasný limit úvěru a rozsahy dat. Název se zobrazí automaticky.

3. Zadejte nový limit úvěru, kterým chcete nahradit aktuální limit úvěru.
4. V polích **Nové počáteční datum** a **Nové konečné datum** určete dobu, kdy je platný rozšířený limit úvěru. Při vytvoření deníku úpravy limitu úvěru je nutné zadat data vypršení platnosti limitu úvěru.

V poli **Stav schválení** je uveden stav workflow řádku deníku.

## <a name="generate-credit-limit-adjustments"></a>Generování úprav limitu úvěru

Limity úvěru je také možné upravit automaticky. V podokně Akce zvolte možnost **Generovat** a poté vyberte jednu z následujících možností:

- Z existujícího odběratele
- Z existující skupiny odběratelů podle limitu úvěru
- Automatické úvěrové limity

### <a name="from-existing-customer"></a>Z existujícího odběratele

Řádky deníku lze vytvářet z existujících odběratelů. Zvolíte-li možnost **Generovat \> z existujícího odběratele**, zobrazí se dialogové okno, v němž můžete zadat kritéria pro výběr odběratelů a výpočet nových limitů.

1. Chcete-li přičíst nebo odečíst částku od limitu úvěru, zadejte hodnotu úpravy. Zadejte zápornou hodnotu, chcete-li snížit aktuální limit úvěru, nebo kladnou hodnotu, chcete-li limit zvýšit.
2. V poli **Typ hodnoty** vyberte způsob, jakým se má při výpočtu nového limitu úvěru použít hodnota zadaná v kroku 1:

    - Chcete-li změnit limit úvěru o určitou částku, vyberte možnost **Pevná hodnota**.
    - Chcete-li změnit limit úvěru o procentní hodnotu, zvolte možnost **Procentní hodnota**.

3. Zadejte hodnotu, která se použije k zaokrouhlení vypočteného limitu úvěru. Chcete-li například zaokrouhlit limit úvěru na nejbližších 10,00 jednotek měny, zadejte **10,00**.
4. Nastavením pole **Způsob zaokrouhlování** určete, zda má být zůstatek zaokrouhlen nahoru nebo dolů.
5. Vyberte metodu, která se používá k úpravě dat.

    - Pokud vyberete možnost **Absolutní**, můžete zadat data definující rozsah dat pro limit úvěru.
    - Pokud vyberete možnost **Relativní**, můžete zadat odchylky data pro daný rozsah. Aktuální rozsah dat pro limit úvěru bude upraven podle odchylky.

6. Pomocí pevné záložky **Záznamy k zahrnutí** lze filtrovat seznam odběratelů, kteří mají být zahrnuti. Pokud filtry nezahrnete, budou vygenerovány položky limitu úvěru pro všechny odběratele.
7. Kliknutím na tlačítko **OK** můžete vytvořit položky úpravy limitu úvěru.

### <a name="from-existing-customer-credit-group"></a>Z existující skupiny odběratelů podle limitu úvěru

Můžete vytvořit řádky deníku z existujících skupin odběratelů podle limitu úvěru. Zvolíte-li možnost **Generovat \> Z existující skupiny odběratelů podle limitu úvěru**, zobrazí se dialogové okno, v němž můžete zadat kritéria pro výběr skupin odběratelů podle limitu úvěru a výpočet nových limitů. Kritéria jsou stejná jako kritéria, která se používají k vytváření řádků deníku z existujících odběratelů. Přečtěte si postup uvedený v předchozí části.

### <a name="automatic-credit-limits"></a>Automatické úvěrové limity

Můžete vytvořit automatické limity úvěru pro definování a aktualizaci limitů úvěrů odběratelů. Automatické limity úvěru se vytvářejí pro skupinu podle rizika a jsou založeny na specifických hodnotách, které se používají ve skupinách podle hodnocení. Tyto automatické limity úvěru lze použít ke generování položek limitu úvěru. Pokud byl odběratel přiřazen ke konkrétní skupině podle rizika a informace o úvěru odběratele odpovídají kritériím pro automatický limit úvěru, je vytvořena položka úpravy limitu úvěru.

#### <a name="create-automatic-credit-limits"></a>Vytvoření automatických limitů úvěru

Automatické limity úvěru se vytvářejí pomocí úprav limitu úvěru. Vyberete-li možnost **Generovat \>Automatické limity úvěru**, zobrazí se dialogové okno, ve kterém můžete nastavit datum vypršení platnosti pro nové limity úvěru, které budou vytvářeny na základě skupin podle rizika, ke kterým jsou odběratelé přiřazeni. Po dokončení klepněte na **OK** a vytvořte řádky úpravy limitu úvěru.

### <a name="post-adjustments"></a>Úpravy zaúčtování

Po vytvoření řádků úpravy limitu úvěru můžete pomocí tlačítka **Zaúčtovat** v podokně Akce zaúčtovat položky a aktualizovat limity úvěrů odběratelů. Pokud jste však nastavili workflow, je nutné v podokně Akce vybrat možnost **Workflow \> Odeslat** a odeslat deník ke schválení.

### <a name="credit-limit-adjustments-workflows"></a>Workflow úprav limitu úvěru

Workflow **Úpravy limitu úvěru** lze použít k odeslání úprav limitu úvěru prostřednictvím procesu schválení workflow. Na stránce **Workflow správy úvěru** (**Správa úvěru \> Nastavení \> Workflow správy úvěru**) můžete vytvořit dvě workflow:

- **Úpravy limitu úvěru** – Toto workflow lze použít ke schválení položek na úrovni záhlaví.
- **Řádek úprav limitu úvěru** – Toto workflow lze použít ke schválení položek úprav, takže položky mohou být schváleny různými lidmi na základě kritérií v rámci workflow.

> [!NOTE]
> Při vytvoření workflow **Úpravy limitu úvěru** můžete workflow nastavit tak, aby se úpravy automaticky zaúčtovávaly po schválení řádků. Pouze do workflow zahrňte úlohu **Automaticky zaúčtovat deník**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]