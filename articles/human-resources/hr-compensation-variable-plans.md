---
title: Vytvoření plánů variabilní kompenzace
description: Variabilní kompenzace tvoří nestandardní mzdu zaměstnance, jako jsou například mzdové bonusy nebo odměny v akciích. Tento článek popisuje součásti, které je nutné nastavit před použitím variabilní kompenzace a přihlášení zaměstnance k plánu variabilní kompenzace.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 4bf2c6525f245a72811f4f239479be360c0c434c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465647"
---
# <a name="create-variable-compensation-plans"></a>Vytvoření plánů variabilní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Variabilní kompenzace tvoří nestandardní mzdu zaměstnance, jako jsou například mzdové bonusy nebo odměny v akciích. Tento článek popisuje součásti, které je nutné nastavit před použitím variabilní kompenzace a přihlášení zaměstnance k plánu variabilní kompenzace.

Výpočet částek variabilní kompenzace pro zaměstnance lze založit na několika faktorech, například na výkonu zaměstnance, úrovni kompenzace zaměstnance nebo výkonnosti oddělení.

## <a name="variable-compensation-components"></a>Komponenty variabilní kompenzace
### <a name="create-compensation-types"></a>Vytvoření typů kompenzaci

**Typy variabilních kompenzací** jsou požadovaný komponent. Typy variabilních kompenzací vám umožňují popsat typy variabilní kompenzace, které vaše organizace odměňuje. Také vám umožňují určit, zda proběhne kompenzace v hotovosti nebo v nepeněžní formě, například jako zásoba.

### <a name="describe-vesting-rules"></a>Popis pravidel připsání

V případě potřeby mohou společnosti nastavit **pravidla připsání**. Pravidla připsání popisují, jak má být časově přidělena variabilní odměna. Pravidlo připsání může například uvádět, že zaměstnanec získá 25 procent své celkové odměny každoročně příští čtyři roky. Pravidla připsání mají pouze informativní charakter.

## <a name="variable-compensation-plans"></a>Plány variabilní kompenzace
**Plán variabilní kompenzace** obsahuje pravidla, metody výpočtu a výchozí hodnoty pro výpočet variabilní kompenzace pro přihlášené zaměstnance. Při vytváření plánu variabilní kompenzace je nutné nastavit typ variabilní kompenzace. Typ variabilní kompenzace určuje, zda systém vypočítá jako odměnu měnovou částku nebo počet jednotek. Dále je nutné nastavit způsob výpočtu:

-   **Časový okamžik** – výpočet variabilní odměny na základě fixní kompenzace, kterou zaměstnanec měl k určitému datu. Toto datum je určeno v procesu události, když se nové částky kompenzace zpracovávají.
-   **Složený** – částka odměny se vypočítá pro každou jedinečnou sazbu mzdy fixní kompenzace, kterou zaměstnanec měl mezi počátečním a koncovým datem cyklu v rámci události procesu. Sazby se poté sečtou k určení výsledné odměny. Během cyklu například zaměstnanec přejde na jiné místo, které má jinou mzdovou sazbu. V takovém případě se variabilní odměna upraví pro délku doby, po kterou byl zaměstnanec v každé mzdové sazbě.

Částka variabilní odměny může být založena buď na procentu pravidelných základních příjmů zaměstnance, nebo pevném počtu jednotek.

-   Vyberte možnost **Procento základu**, zadejte výchozí procento a určete, zda má být základ pevná mzdová sazba zaměstnance nebo kontrolní bod úrovně kompenzace zaměstnance. Úroveň kompenzace se nastavuje u pozice zaměstnance. Jeden z referenčních bodů ze struktury kompenzace můžete nastavit jako kontrolní bod v plánu fixní kompenzace. Systém použije úroveň kompenzace z pozice zaměstnance a vytvoří křížový odkaz s kontrolním bodem, který je uveden v zaměstnancově plánu fixní kompenzace, aby zjistil částku kontrolního bodu pro úroveň kompenzace zaměstnance. Částka kontrolního bodu se pak použije namísto pevné mzdové sazby zaměstnance jako základ pro odměnu.
-   Vyberte možnost **Počet jednotek** a zadejte výchozí počet jednotek, hodnotu každé jednotky a měnu jednotkové hodnoty v případě, že plán kompenzace je pro bezhotovostní odměnu (například 200 jednotek zásob je oceněno na 40 USD), nebo pouze počet jednotek, pokud je plán kompenzace pro finanční odměnu. Pro finanční odměnu zaměstnanec obdrží určený počet jednotek měny, který je použitý pro jeho plán fixní kompenzace (například 500 jednotek po 1 USD). Ovládací prvek vztahu jedna ku jedné lze použít k určení, zda je přímé mapování jedna ku jedné mezi počtem jednotek a jednotkovou hodnotou. Při vytváření plánu variabilní kompenzace pro plán hotovosti na základě počtu jednotek je tato možnost automaticky nastavená na **Ano** a jednotková hodnota je **1.0000**.

Nastavení položky **Pravidlo zařazení** umožňuje určit, zda mají všichni zaměstnanci získat stejné zvýšení bez ohledu na datum, kdy byli přijati (**Pravidlo** = **Žádné**), nebo zda mají získat procentuální odměnu podle toho, jak dlouho jsou v cyklu zaměstnáni (**Pravidlo zařazení** = **Procento**). 

**Účinek** umožňuje upravit odměnu zaměstnance na základě výkonnosti jeho oddělení. Měřítka výkonnosti lze nastavit pro každé oddělení na stránce **Oddělení** v části **Související formuláře** &gt; **Kompenzace** &gt; **Výkonnost**. Odměna, kterou zaměstnanci oddělení získají, závisí na hodnotě v poli **Dosažená procentuální část cíle**, která označuje výkonnost oddělení:

-   Je-li výkonnost oddělení 100 %, odměna pro zaměstnance oddělení se promítne podle procenta, které se nastavuje v poli **Výběr na 100 %**.
-   Pokud je výkonnost oddělení více než 100 %, systém přidá sazbu, která se nastavuje v poli **Na procento nad cílem**, k procentům v poli **Výběr na 100 %**, dokud se nedosáhne hodnoty v poli **Nejvyšší povolený výběr**.
-   Pokud je výkonnost oddělení méně než 100 %, systém odečte sazbu, která se nastavuje v poli **Na procento pod cílem**, od procent v poli **Výběr na 100 %**, dokud se nedosáhne hodnoty v poli **Nejnižší povolený výběr**.

Můžete nastavit **úrovně tolerance** na prahovou hodnotu procent, takže se zobrazí varovná zpráva, pokud účinek dosadí procentuální hodnotu mimo prahovou procentuální hodnota. 

Ve výchozím nastavení systém vyhledá oddělení, které je nastaveno u pozice zaměstnance. Odměny pro některé zaměstnance však mohou záviset na výkonnosti více oddělení. V takovém případě lze různá oddělení a procentuální odměny přidělené k výkonnosti každého oddělení nastavit na přihlášení variabilní kompenzace zaměstnance. Další informace naleznete v části „Přihlášení variabilní kompenzace" v následujícím oddílu. 

Účinek se používá jen při označení volby **Výkonnostní složka** při spuštění procesu kompenzace. 

Karta **Úrovně přepsání** umožňuje přepsat výchozí hodnotu odměny v procentech nebo počtu jednotek na základě úrovně kompenzace zaměstnance. Pokud je volba **Povolit přepisy pro úrovně** nastavena na hodnotu **Ano** pro zaměstnance přihlášené v plánu variabilní kompenzace, systém použije úroveň z pozice zaměstnance, a poté ji vyhledá v tabulce úrovní přepsání, aby určil procentuální hodnotu nebo počet jednotek pro tuto úroveň. Pokud úroveň nebyla nalezena v tabulce úrovní přepsání, použije se výchozí procento nebo počet jednotek z karty **Obecné**. Procento a počet jednotek lze také přepsat na přihlášení zaměstnance v plánu variabilních kompenzací.

## <a name="variable-compensation-enrollment"></a>Přihlášení variabilní kompenzace
### <a name="determine-who-is-eligible-for-the-plan"></a>Určení osob způsobilých pro plán

Když jste připraveni přihlásit zaměstnance do plánu variabilní kompenzace, nejprve určete, kdo má nárok na kompenzaci specifikovanou v plánu. Dokud způsobilost neurčíte, nebude možné přiřadit k plánu zaměstnance. Chcete-li nárok nastavit, otevřete stránku **Pravidla způsobilosti** a vytvořte nové pravidlo způsobilosti pro plán. Poté definujte kritéria, která musí zaměstnanec splňovat, aby měl na kompenzační plán nárok. Způsobilost můžete omezit podle oddělení, odborů, oblasti kompenzace (umístění), pracovní pozice, pracovní funkce, typu práce a/nebo úrovně kompenzace. Zaměstnance lze zařadit do plánu kompenzace pouze v případě, že splňují **všechna** kritéria, která jsou nastavena pro pravidlo způsobilosti. 

**Poznámka:** Pravidla způsobilosti se používají pro určení způsobilosti u fixních kompenzačních plánů a variabilních kompenzačních plánů. Pravidlo způsobilosti používá následující pole v záznamech práce, pozice a zaměstnanec a určí, zda je zaměstnanec způsobilý pro kompenzační plán:

- Na stránce **Práce**:
  -   Pole **Práce**
  -   Pole **Funkce** a **Typ práce** na kartě **Klasifikace práce**
  -   Pole **Úroveň** na kartě **Kompenzace**
- Na stránce **Pozice**: pole **Oddělení** a **Oblast kompenzace**.
- Na stránce <strong>Zaměstnanci</strong>: informace o odborech přiřazených k zaměstnanci jsou v části <strong>Osobní údaje</strong> &gt; <strong>Odbory</strong> na kartě *<strong><em>Pracovník</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Povolení zařazení do plánu variabilní kompenzace

Na stránce **Plány variabilní kompenzace** nastavte volbu **Povolit přihlášení** na hodnotu **Ano**, abyste umožnili zaměstnancům přihlášení do plánu.

### <a name="enroll-the-employee"></a>Přihlášení zaměstnance

Nyní můžete zařadit zaměstnance do plánu variabilní kompenzace. Chcete-li zaměstnance zařadit, přejděte na stránku **Zaměstnanci** a vyberte zaměstnance. V podokně akcí klikněte na tlačítko **Kompenzace** &gt; **Zápis variabilního plánu**. 

**Poznámka:** volba **Přihlášení** musí být nastavena na hodnotu **Ano** v plánu variabilní kompenzace. Pole **Plán** zobrazí jen ty plány, pro které je zaměstnanec způsobilý na základě pravidel způsobilosti nastavených pro tyto plány. Není-li pro plán nastaveno žádné pravidlo způsobilosti, nebude pro něj způsobilý žádný zaměstnanec. 

Ujistěte se, že pole **Datum platnosti** je nastaveno správně. Používá-li plán variabilní kompenzace metodu výpočtu **Složený**, datum platnosti zařazení může být zvažováno během výpočtu odměny pro zaměstnance. 

Lze použít kartu **Přepsání** a přepsat specifické hodnoty pro zaměstnance. Například pokud je **Pravidlo zařazení** nastaveno v plánu na hodnotu **Procento** a jiné datum přijetí se má použít při výpočtu procentuální části náboru zaměstnance, můžete nastavit datum náboru v poli **Datum pravidla zařazení**. Je také možné přepsat buď hodnotu **Procentuální odměna**, nebo hodnotu **Počet jednotek** pro určitého zaměstnance v závislosti na nastavení plánu. Tyto hodnoty se stále promítnou do pravidla zařazení, výkonnostních faktorů a jiných nastavení v plánu. 

**Organizační přepsání** se používají k založení odměny pro zaměstnance na výkonnosti jednoho nebo více oddělení. Procenta, která se rozdělují mezi oddělení, musí v součtu činit 100 procent. Individuální výkonnost zaměstnance se také bere v potaz. Tato nastavení se používají pouze v případě, že je zvolena možnost **Výkonnostní složka** při spuštění procesu kompenzace.





[!INCLUDE[footer-include](../includes/footer-banner.md)]