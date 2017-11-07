---
title: "Generování sestav v rámci zákona o cenově dostupné zdravotní péči (Affordable Care Act)"
description: "Tato funkce má pomáhat zaměstnavatelům, kteří potřebují sledovat informace ve formulářích 1095-B a 1095-C v rámci zmocnění zaměstnavatele v kontextu zákona Affordable Care Act (ACA). Tato funkce je povolena pouze pro právnické osoby v USA."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e529eb4712087f7af9e3179340c2f00524555b3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="generate-affordable-care-act-reports"></a>Generování sestav v rámci zákona o cenově dostupné zdravotní péči (Affordable Care Act)
Tato funkce má pomáhat zaměstnavatelům, kteří potřebují sledovat informace ve formulářích 1095-B a 1095-C v rámci **zmocnění zaměstnavatele** v kontextu zákona Affordable Care Act (ACA). Tato funkce je povolena pouze pro právnické osoby v USA.

## <a name="getting-started"></a>Začínáme
Při sledování informací uvedených ve formulářích 1095-B a 1095-C je nutné nejprve vytvořit jednu nebo více skupin pokrytí pro ACA. Tyto skupiny se použijí k označení nabídky pokrytí nabídnuté zaměstnanci, zaměstnancova podílu na měsíční náhradě s nejnižšími náklady (pokud je tato cena vyšší než federální hranice chudoby) a případně také programu Safe Harbor, který zaměstnavatel používá. Pokud použijete skupiny pokrytí ACA, budete moci informace v těchto polích spravovat hromadně a nebudete muset upravovat každý záznam zaměstnance se stejnými podmínkami. Skupiny pokrytí ACA lze navíc snadno přiřadit k jednomu nebo několika zaměstnancům pomocí funkce hromadného přiřazení na stránce.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Správa několika verzí skupiny pokrytí
Můžete používat několik verzí skupin pokrytí a provádět průběžně aktualizace, aniž by bylo nutné vytvářet nové skupiny a přeřazovat do ní zaměstnance při každé změně v organizaci nebo v nabízených výhodách. 

Po vytvoření potřebných skupin pokrytí ACA je můžete hromadně přiřadit k zaměstnancům pomocí funkce **Hromadné přiřazení** na stránce. Můžete také u jednotlivých zaměstnanců nastavit, zda je u nich třeba sledovat a vykazovat informace o ACA, a můžete je jednotlivě přiřazovat ke skupinám pokrytí ACA.

Pokud u některého zaměstnance není nutné sledovat nebo vykazovat informace v rámci ACA (například jde-li o zaměstnance na částečný úvazek), je možné nastavit pole **Vykazovat pokrytí** na možnost Ne. Všichni zaměstnanci, u kterých je třeba sledovat informace ACA, musí být přiřazeni k některé skupině pokrytí ACA. Přesto však můžete měnit možnosti **Nabídka pokrytí**, **Podíl zaměstnance na nákladech** a **Dohoda Safe Harbor** u všech měsíců, které vyžadují zadání jiných hodnot, než jaké jsou uvedeny ve skupině pokrytí.

Chcete-li zadat výjimky z hodnot skupiny pokrytí ACA, klikněte na odkaz pokrytí ACA na stránce podrobností pracovníka (v části Další informace na kartě Zaměstnání).

## <a name="reporting-health-care-coverage"></a>Vykazování pokrytí zdravotní péče
Pokud zaměstnavatel nabízí sponzorované pokrytí s vlastním připojištěním a zaměstnanec tuto nabídku využívá (bez ohledu na to, zda pracuje na plný nebo částečný úvazek), je ve formuláři 1095-C nutné hlásit i další informace vedle údajů o tom, jaké (pokud nějaké) pokrytí zdravotního pojištění bylo nabídnuto zaměstnanci na plný úvazek. Ve výkazu musí být uvedeni všichni zaměstnanci (včetně závislých osob) krytí v rámci plánů zaměstnaneckých výhod sponzorovaných zaměstnavatelem, a to ve všech měsících, kdy pokrytí platilo. 

Zaškrtnutím políčka **Lze vykázat podle zákona o dostupné péči** můžete určit, zda je třeba daný plán zaměstnaneckých výhod vykazovat.

Pokud si zaměstnanci navíc zvolili i krytí závislých osob, je možné uvést data, kdy pokrytí začalo platit, na stránce Udržovat výhody. Chcete-li uvést, že se výhoda vztahuje na závislou osobu, vyberte tlačítko Upravit na panelu akcí na kartě Rodinní příslušníci.

Na stránce **Správce dat pokrytí rodinného příslušníka** můžete určit data pokrytí závislých osob v rámci zaměstnanecké výhody. Zadáním data na této stránce automaticky zaškrtnete políčko **Pokryto** na stránce **Udržovat výhody**.

## <a name="generate-1095b-and-1095c-forms"></a>Generování formulářů 1095-B a 1095-C
Formuláře 109-B and 1095-C můžete vygenerovat i v aplikaci a rozeslat je všem zaměstnancům. V systému lze také elektronicky vygenerovat formuláře 1095-C a odpovídající soubory pro přenos 1094-C, které lze poslat na finanční úřad.  

Při generování formuláře 1095-C zadejte příslušný kalendářní nebo daňový rok a uveďte, zda chcete vytisknout dvoustránkový nebo třístránkový formulář. Třístránkový formulář je nutný pouze v případě, že zaměstnavatel poskytoval pokrytí s vlastním pojištěním a zaměstnanec má více než šest pokrytých závislých osob (včetně sebe). Při generování dvoustránkového formuláře systém automaticky zjistí, zda má zaměstnanec více než šest pokrytých závislých osob, a nebude tohoto zaměstnance při generování formuláře zahrnovat. Kromě toho při generování třístránkového formuláře systém zahrne jen zaměstnance s více než šesti pokrytými závislými osobami.

## <a name="viewing-information"></a>Zobrazení informací
Pomocí stránky **Pokrytí dostupné péče pro pracovníka** můžete zjistit, kteří zaměstnanci byli přiděleni k jednotlivým skupinám pokrytí, kteří zařazeni být nemusí a kteří přiřazeni nejsou.

U případných přepsaných výchozích hodnot skupiny pokrytí ACA se vedle změněné hodnoty zobrazí hvězdička. Pokud jsou hodnoty u všech 12 měsíců stejné a nebyly přepsány, hodnota bude uvedena ve sloupci **Všech 12 měsíců**.

Pomocí okna dotazu můžete zjistit, u kterých zaměstnanců bylo určeno, že se nemají v rámci ACA vykazovat (to znamená, že není třeba sledovat, zda jim bylo nabídnuto pokrytí, a není pro ně třeba na konci roku vydávat formulář 1095-C). Výběrem možnosti **Nelze vykázat podle zákona o dostupné péči** v poli **Filtrovat podle** můžete vytvořit seznam všech zaměstnanců, na které se nevztahuje formulář 1095-C.

Kromě zobrazení seznamu zaměstnanců, na které se vykazování podle ACA nevztahuje, můžete také zobrazit všechny zaměstnance, kteří nejsou přiřazeni (pole **Vykazovat pokrytí ACA** je prázdné) nebo kteří byli přiřazeni do skupiny pokrytí ACA, jejíž platnost pro rok zadaný v poli **Rok** vypršela.

Seznamy zaměstnanců vygenerovaných podle zadaných filtrů je možné exportovat do aplikace Excel.

Pokud je nutné vykazovat pokryté osoby, protože jako zaměstnavatel poskytujete pokrytí s vlastním pojištěním, můžete zobrazit i všechny závislé osoby kryté v rámci plánů zaměstnaneckých výhod a označené jako **Lze vykázat podle zákona o dostupné péči** výběrem akce Zobrazit pokrytí závislých prvků na panelu akcí.

**Poznámka:** V okně dotazu se zobrazí pouze zaměstnanecké výhody, jejichž plán byl označen jako **Lze vykázat podle zákona o dostupné péči**.

