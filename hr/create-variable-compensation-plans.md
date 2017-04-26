---
title: "Vytvoření plánů variabilní kompenzace"
description: "Variabilní kompenzace tvoří nestandardní mzdu zaměstnance, jako jsou například mzdové bonusy nebo odměny v akciích. Toto téma popisuje součásti, které musí být nastavena předtím, než můžete použít variabilní kompenzace a zapsat do plánu variabilní kompenzace zaměstnance."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Vytvoření plánů variabilní kompenzace

[!include[banner](includes/banner.md)]


Variabilní kompenzace tvoří nestandardní mzdu zaměstnance, jako jsou například mzdové bonusy nebo odměny v akciích. Tento článek popisuje součásti, které je nutné nastavit před použitím variabilní kompenzace a přihlášení zaměstnance k plánu variabilní kompenzace.

Výpočet částek variabilní kompenzace pro zaměstnance lze založit na několika faktorech, například na výkonu zaměstnance, úrovni kompenzace zaměstnance nebo výkonnosti oddělení.

## <a name="variable-compensation-components"></a>Komponenty variabilní kompenzace
### <a name="create-compensation-types"></a>Vytvoření typů kompenzaci

**Typy variabilních kompenzací **jsou požadovaný komponent. Typy variabilních kompenzací vám umožňují popsat typy variabilní kompenzace, které vaše organizace odměňuje. Také vám umožňují určit, zda proběhne kompenzace v hotovosti nebo v nepeněžní formě, například jako zásoba.

### <a name="describe-vesting-rules"></a>Popis pravidel připsání

V případě potřeby mohou společnosti nastavit **pravidla připsání**. Pravidla připsání popisují, jak by měly být přidělovány variabilní odměny v průběhu času. Například pravidlo připsání může stát, že zaměstnanec obdrží 25 % své celkové odměny každý rok další čtyři roky. Pravidla připsání jsou pouze informativní.

## <a name="variable-compensation-plans"></a>Plány variabilní kompenzace
**Plán variabilní kompenzace** obsahuje pravidla, metody výpočtu a výchozí hodnoty pro výpočet variabilní kompenzace pro přihlášené zaměstnance. Po vytvoření plánu variabilní kompenzace, je nutné nastavit typ variabilní kompenzace. Typ variabilní kompenzace Určuje, zda systém vypočítá částku měny nebo počet jednotek jako nálezu. Dále je nutné nastavit způsob výpočtu:

-   **Kdykoli** – výpočet variabilní odměny vychází z fixní kompenzace, která má zaměstnance k určitému datu. Toto datum je určeno na procesní události při zpracování nové částky kompenzace.
-   **Složený** – částka odměny se vypočítá pro každou jedinečnou sazbu mzdy fixní kompenzace, kterou zaměstnanec měl mezi počátečním a koncovým datem cyklu v rámci události procesu. Sazby jsou potom přidány společně k určení konečného nálezu. Během cyklu, například zaměstnanec převeden do jiné polohy, která měla jinou sazbu. V takovém případě se variabilní odměna upraví pro délku doby, po kterou byl zaměstnanec v každé mzdové sazbě.

Částka variabilní odměny může být založena buď na procentu pravidelných základních příjmů zaměstnance, nebo pevném počtu jednotek.

-   Vyberte možnost **Procento základu**, zadejte výchozí procento a určete, zda má být základ pevná mzdová sazba zaměstnance nebo kontrolní bod úrovně kompenzace zaměstnance. Úroveň kompenzace je nastavit úlohy zaměstnance. Jeden z referenčních bodů ze struktury kompenzace můžete nastavit jako řídicí bod na plán fixní kompenzace. Systém použije úroveň kompenzace z práce zaměstnance a vytvořit křížový odkaz s řídicí bod, který je uveden na plán fixní kompenzace zaměstnance ke zjištění částky ovládací bod pro úroveň kompenzace zaměstnance. Velikost bodu ovládacího prvku se potom použije místo pevné mzdové sazby zaměstnance jako základ pro zadávání.
-   Vyberte možnost **Počet jednotek** a zadejte výchozí počet jednotek, hodnotu každé jednotky a měnu jednotkové hodnoty v případě, že plán kompenzace je pro bezhotovostní odměnu (například 200 jednotek zásob je oceněno na 40 USD), nebo pouze počet jednotek, pokud je plán kompenzace pro finanční odměnu. Pro hotovostní ocenění obdrží zaměstnanec určený počet jednotek měny, který se používá pro svůj plán fixní kompenzace (například 500 jednotek 1 USD). Vztah 1: 1 prvek lze použít k označení, zda je přímé mapování 1: 1 mezi počet jednotek a jednotková hodnota. Při vytvoření plánu variabilní kompenzace pro plán na základě hotovosti pomocí počtu jednotek, je tato možnost automaticky uzamčen na **Ano**, a je jednotková hodnota **1.0000**.

**Pravidla zařazení** nastavení umožňuje určit, zda všechny zaměstnance, by měl dostat stejné zvýšení, a to bez ohledu na datum, které byly přijaty (**pravidla zařazení** = **žádný**), nebo zda zaměstnanci měli obdržet procento odměny, která je na základě délky jejich zaměstnání během cyklu (**pravidla zařazení** = **%**). 

**Účinek** umožňuje upravit odměny zaměstnance, na základě výkonu zaměstnance oddělení. Měřítka lze nastavit pro každé oddělení na **oddělení** stránky v **souvisejících formulářů**&gt;**kompenzace**&gt;**výkon**. Odměny, kterou zaměstnanci tohoto oddělení závisí na hodnotě **procent dosaženo cíle** pole, což znamená výkon oddělení:

-   Je-li výkonnost oddělení 100 %, odměna pro zaměstnance oddělení se promítne podle procenta, které se nastavuje v poli **Výběr na 100 %**.
-   Pokud je výkonnost oddělení více než 100 %, systém přidá sazbu, která se nastavuje v poli **Na procento nad cílem**, k procentům v poli **Výběr na 100 %**, dokud se nedosáhne hodnoty v poli **Nejvyšší povolený výběr**.
-   Pokud je výkonnost oddělení méně než 100 %, systém odečte sazbu, která se nastavuje v poli **Na procento pod cílem**, od procent v poli **Výběr na 100 %**, dokud se nedosáhne hodnoty v poli **Nejnižší povolený výběr**.

Můžete nastavit** úrovně tolerance** na prahovou hodnotu procent, takže se zobrazí varovná zpráva, pokud účinek dosadí procentuální hodnotu mimo prahovou procentuální hodnota. 

Ve výchozím nastavení systém jej vyhledá oddělení, které je nastaveno na postavení zaměstnanců. Odměny pro některé zaměstnance však může záviset na výkonu více útvarů. V tomto případě různá oddělení a procento odměny, která je přidělena k výkonu jednotlivých oddělení lze nastavit na přihlášení variabilní kompenzace zaměstnance. Další informace naleznete v části "přihlášení variabilní kompenzace", který následuje. 

Účinek se používá jen při označení volby **Výkonnostní složka** při spuštění procesu kompenzace. 

**Hladiny přepisy** karta umožňuje přepsat výchozí procento nebo počet jednotek, podle úrovně kompenzace zaměstnance o udělení. Pokud **povolit přepsání pro úrovně** je nastavena na **Ano** pro zaměstnance, kteří jsou zaregistrováni v plánu variabilní kompenzace, systém má úroveň z práce zaměstnance a potom vyhledá ji v úrovni přepíše tabulky určete procentuální hodnotu nebo počet jednotek pro danou úroveň. Pokud není nalezen na úrovni v úrovni přepíše tabulka, výchozí procento nebo počet jednotek z **Obecné** karta se používá. Procento a počet jednotek lze také přepsat u přihlášení zaměstnance plánu variabilní kompenzace.

## <a name="variable-compensation-enrollment"></a>Přihlášení variabilní kompenzace
### <a name="determine-who-is-eligible-for-the-plan"></a>Určení osob způsobilých pro plán

Když jste připraveni přihlásit zaměstnance do plánu variabilní kompenzace, nejprve určete, kdo má nárok na kompenzaci specifikovanou v plánu. Dokud způsobilost neurčíte, nebude možné přiřadit k plánu zaměstnance. Chcete-li nárok nastavit, otevřete stránku **Pravidla způsobilosti** a vytvořte nové pravidlo způsobilosti pro plán. Poté definujte kritéria, která musí zaměstnanec splňovat, aby měl na kompenzační plán nárok. Způsobilost můžete omezit podle oddělení, odborů, oblasti kompenzace (umístění), pracovní pozice, pracovní funkce, typu práce a/nebo úrovně kompenzace. Zaměstnance lze zařadit do plánu kompenzace pouze v případě, že splňují **všechna** kritéria, která jsou nastavena pro pravidlo způsobilosti. 

**Poznámka:** Pravidla způsobilosti se používají pro určení způsobilosti u fixních kompenzačních plánů a variabilních kompenzačních plánů. Pravidlo způsobilosti používá následující pole v záznamech práce, pozice a zaměstnanec a určí, zda je zaměstnanec způsobilý pro kompenzační plán:

-   Na stránce **Práce**:
    -   Pole **Práce**
    -   Pole **Funkce** a **Typ práce** na kartě **Klasifikace práce**
    -   Pole **Úroveň** na kartě **Kompenzace**
-   Na stránce **Pozice**: pole **Oddělení** a **Oblast kompenzace**.
-   Na **zaměstnanci** stránky: informace o odbory, který je přidružen zaměstnance podle **osobní údaje**&gt;**odbory** na *** karta pracovníka ***

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Povolení zařazení do plánu variabilní kompenzace

Na stránce **Plány variabilní kompenzace** nastavte volbu **Povolit přihlášení** na hodnotu **Ano**, abyste umožnili zaměstnancům přihlášení do plánu.

### <a name="enroll-the-employee"></a>Přihlášení zaměstnance

Nyní můžete zařadit zaměstnance do plánu variabilní kompenzace. Chcete-li zaměstnance zařadit, přejděte na stránku **Zaměstnanci** a vyberte zaměstnance. V podokně akcí klepněte na tlačítko **kompenzace**&gt;**Zápis variabilního plánu**. 

**Poznámka:** volba **Přihlášení** musí být nastavena na hodnotu **Ano** v plánu variabilní kompenzace. **Plán** pole zobrazí pouze plány, které je zaměstnanec způsobilý pro založené na pravidla způsobilosti, které jsou nastaveny pro tyto plány. Pokud není pravidla způsobilosti pro plán, žádní zaměstnanci budou způsobilé pro tento plán. 

Ujistěte se, že **datum účinnosti** je nastaveno správně. Pokud používá plánu variabilní kompenzace **složené** metoda výpočtu, datum platnosti přihlášení mohly být považovány za při výpočtu odměny zaměstnance. 

Lze použít **přepíše** kartu a přepsat hodnoty specifické pro zaměstnance. Například pokud **pravidla zařazení** je nastavena na **%** v plánu a jiné cizí data se použije během výpočtu Procento zařazení zaměstnance, můžete nastavit datum přijetí v **datum pravidla zařazení** pole. Je také možné přepsat buď **procento odměny** hodnoty nebo **počet jednotek** hodnota pro určitého zaměstnance, v závislosti na nastavení plánu. Tyto hodnoty budou zahrnuty stále pravidla zařazení, faktory výkonu a další nastavení plánu. 

**Organizační přepsání** lze založit na výkonu jednoho nebo více útvarů ocenění zaměstnance. Procento, které je přiděleno přes oddělení by měla dohromady 100procent $2. Je také považován za výkonu pro jednotlivé zaměstnance. Tato nastavení se použijí pouze tehdy, pokud **výkonnostní** je vybrána při spuštění procesu kompenzace.

<a name="see-also"></a>Viz také
--------

[Plány kompenzace](compensation-plans.md)




