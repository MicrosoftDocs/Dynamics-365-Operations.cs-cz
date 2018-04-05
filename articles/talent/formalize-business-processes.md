---
title: "Formalizace obchodních procesů"
description: "Funkce Obchodní proces vám umožňuje vytvořit šablonu obchodního procesu pro procesy, které je třeba dokončit v rámci vaší organizace."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: cs-cz
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Formalizace obchodních procesů
Funkce Obchodní proces vám umožňuje vytvořit šablonu obchodního procesu pro procesy, které je třeba dokončit v rámci vaší organizace. Vaše společnost může například provést personální audit každého roku. Je možné vytvořit šablonu ke sledování všech úkolů, které audit obsahuje, chcete-li zajistit, aby všechny úlohy byly prováděny pokaždé, když je proces dokončen, a pokud je to nutné, aby bylo zajištěno, že jsou úlohy prováděny úlohy ve správném pořadí. Šablony lze znovu použít pro opakované procesy nebo zkopírovat pro použití jako výchozího bodu při vytváření nových šablon.

Po vytvoření šablony lze proces spustit a sledovat v pracovním prostoru Podnikový proces.  Při spuštění obchodního procesu budou přiřazeny úlohy odpovídajícím osobám a budou obsahovat data splnění. Tyto komponenty popíšeme podrobně dále.

## <a name="business-process-template"></a>Šablona obchodního procesu
Šablona obchodního procesu uvádí skupinu úkolů, které tvoří obchodní proces. Obchodní procesy ve výchozím nastavení mohou vytvářet správci lidských zdrojů a asistenti ve výchozím nastavení.  To lze však upravit v konfiguraci zabezpečení úpravou funkčního oprávnění Udržovat obecné obchodní procesy.

Vlastníka procesu lze definovat pro každý proces.  Vlastník procesu bude mít přehled o všech úlohách procesu a může opětovně přiřadit úkoly nebo změnit datum splatnosti.  Ředitel HR například může vytvořit šablonu obchodního procesu pro dávky revize.  Manažeři kompenzací a zaměstnaneckých výhod mohou být nastaveni jako vlastníci procesu tak, aby měli přehled úkolů, které je třeba dokončit jako součást revize.  Vlastník procesu nemůže vytvořit nebo odstranit aktivní obchodních procesů nebo šablony obchodních procesů.

## <a name="task"></a>Úkol
Obchodní proces často obsahuje více úkolů. Některé úlohy lze dokončit v rámci aplikace Dynamics 365 for Talent[?], jako například kontrolu nabídky interních kurzů. V tomto případě by v poli Propojení úloh byla vybrána položka nabídky. Ostatní úlohy mohou zahrnovat revize nebo vyplňování formuláře na webové stránce. Volba adresy URL v poli Odkaz na úkol povolí webovou adresu, která má být zadána. Pro externí a interní weby můžete v tomto poli zadat adresy URL. Můžete také vytvořit úkoly pro aktivity, které provádíte ručně, například kontrolu přístupu všech struktur. V takovém případě není požadováno propojení úloh. Tato flexibilita vám umožňuje sledovat více druhů úloh v komplexním procesu.

Úlohy lze přiřadit konkrétnímu pracovníkovi nebo pozici. Například správce odměňování a zaměstnaneckých výhod bude vždy osoba, která provádí přehled pojistného.   Při vytváření této úlohy vyberte pro tento typ přiřazení pozici a poté vyberte manažera kompenzací a zaměstnaneckých výhod ze seznamu pozic. Po spuštění procesu se přiřadí úloha k pracovníkovi, který je na pozici manažera kompenzací a zaměstnaneckých výhod. Můžete také přiřadit úkol konkrétnímu pracovníkovi výběrem možnosti Pracovník v poli Typ přiřazení a následným zvolením příslušné osoby.

Data splnění úkolů závisí na cílovém datu zadaném na začátku procesu. Některé úlohy musí být dokončeny před cílovým datem a některé mohou být dokončeny po cílovém datu.  Při definování úkolu zadáte datum splatnosti, které je relativní k cílovému datu v posunu data splatnosti z cílového pole data. Předpokládejme například, že správce odměňování a zaměstnaneckých výhod musí provést kontrolu pojištění prémií 10 dní před dokončením auditu lidských zdrojů. Vytvořené úlohy mají datum splatnosti relativní vůči cílovému datu -10. Je-li proces zahájen 13. května, úloha bude mít datum splatnosti 3. května. Poznámka: Data splatnosti lze upravit také po zahájení procesu.

Komplexní úkoly mohou vyžadovat více kroků, nebo aby jednotlivec prováděl úlohy pro poskytnutí dalších informací. Můžete přidat instrukce k úkolu a zahrnout k instrukcím formát RTF. Pokyny mohou poskytovat další informace o tom, jak má úkol dokončit osoba, která je přiřazena k jejímu dokončení.

Spuštění procesu Proces lze spustit v rámci šablony obchodního procesu volbou Spustit proces.  Při zahájení procesu budou vytvořeny úlohy pro vybrané pracovníky anebo pozice, definované v úlohách, které jsou zahrnuty v šabloně obchodních procesů. Každému úkolu bude také přiděleno datum splatnosti bude, přidáním nebo odebráním dnů posunu od cílového data (viz informace týkající se posunu dnů v části úkol). Aktivní obchodní procesy lze zobrazit v pracovním prostoru Obchodní procesy. 

## <a name="employee-self-service"></a>Samoobsluha pro zaměstnance
Když je zaměstnanci přiřazen úkol, lze zobrazit jeho přiřazené úkoly na stránce samoobsluhy pro zaměstnance. Zaměstnanci, kteří mají přidělené úlohy obchodního procesu, mohou zobrazit úlohu, její popis, pokyny pro dokončení a jméno kontaktní osoby a mohou otevírat přidruženou stránku nebo webovou stránku Dynamics365 ze samoobslužné stránky Zaměstnanec. Úlohy lze označit jako probíhající, zrušené nebo dokončené.

## <a name="business-process-workspace"></a>Šablona obchodního procesu
Odborníci na personalistiku mohou zobrazovat aktivní obchodní procesy z pracovní plochy Obchodní proces. Pracovní prostor uvádí seznam všech aktivních procesů a úloh, které jsou přidružené ke každé úloze. Komplexní seznam úloh lze filtrovat podle data splatnosti. Na stránce se zobrazí také úlohy po termínu a úkoly konkrétně přiřazené k odborníkovi lidských zdrojů. Mohou též aktualizovat stav všech úloh a v případě potřeby opětovně přiřadit úlohy pro udržení postupu celkového obchodního procesu.

## <a name="my-business-processes-workspace"></a>Pracovní prostor Moje obchodní procesy
Vlastníci procesu mohou zobrazit aktivní obchodní procesy, které jim jsou přiřazeny z pracovního prostoru Můj obchodní proces. Pracovní prostor uvádí seznam všech aktivních procesů a přidružených úloh, které tento uživatel vlastní.  Komplexní seznam úloh lze filtrovat podle data splatnosti. Na stránce se zobrazí také úkoly konkrétně přiřazené vlastníkovi procesu. Vlastník procesu může také aktualizace stav všech úloh a také opětovně přiřadit všechny úlohy.

## <a name="navigating-business-processes"></a>Procházení obchodních procesů
1.   Chcete-li přidat šablonu obchodních procesů, přejděte na Obchodní procesy - odkazy - Správa obchdoních procesů.
 - a.   Nyní vytvoříme novou šablonu.
 - b.   Kopírování ze šablony zkopíruje vybranou šablonu do nové.
 - c.   Spuštění procesu zahájí vybraný obchodní proces, přiřadí úlohy a vypočítá data splatnosti.  
2.  Chcete-li zobrazit aktivní procesy a přidružené úlohy, přejděte na pracovní prostor Obchodní procesy.

