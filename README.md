import { Button } from "@/components/ui/button";
import { Card } from "@/components/ui/card";
import { Instagram, Linkedin } from "lucide-react";
import React from "react";

export default function Desktop(): JSX.Element {
  // Navigation items
  const navItems = [
    { title: "HOME", href: "#" },
    { title: "ABOUT ME", href: "#" },
    { title: "PORTFOLIO", href: "#" },
    { title: "CONTACT", href: "#" },
  ];

  // Portfolio projects
  const portfolioProjects = [
    { color: "bg-blue-700", image: "HEROSHOT-MIPA-2.png" },
    { color: "bg-[#3cb371]" },
    { color: "bg-[#f24c8e]" },
    { color: "bg-[#ff8c00]" },
  ];

  return (
    <div className="bg-white flex flex-row justify-center w-full">
      <div className="bg-white overflow-hidden w-full max-w-[1440px] relative">
        {/* Header and Hero Section */}
        <header className="relative w-full h-[1040px]">
          {/* Navigation */}
          <nav className="w-full h-[138px] bg-[#ff8c00] flex items-center justify-center">
            <ul className="flex items-center">
              {navItems.map((item, index) => (
                <li key={index} className="w-[294px]">
                  <a
                    href={item.href}
                    className="font-['Roboto_Slab-SemiBold',Helvetica] font-semibold text-[#f5f0e1] text-[35px] text-center block"
                  >
                    {item.title}
                  </a>
                </li>
              ))}
            </ul>
          </nav>

          {/* Hero Content */}
          <div className="w-full h-[902px] bg-[#f5f0e1] flex flex-col items-center justify-center px-4">
            <h1 className="font-['Roboto_Slab-Bold',Helvetica] font-bold text-[#f24c8e] text-[160px] text-center">
              HEY!
            </h1>
            <h2 className="font-['Montserrat-SemiBold',Helvetica] font-semibold text-[#ff8c00] text-[50px] text-center mt-4">
              FIJN JE TE ONTMOETEN
            </h2>
            <p className="font-['Montserrat-Regular',Helvetica] font-normal text-black text-3xl text-center max-w-[967px] mt-6">
              Welkom in een wereld waar kleur en creativiteit samenkomen. Hier
              staan ontwerpen centraal die niet alleen mooi zijn, maar ook
              effectief communiceren. Met aandacht voor detail en een balans
              tussen esthetiek en doelgerichtheid, wordt elk project met zorg
              vormgegeven. Neem gerust de tijd om het werk te ontdekken.
            </p>
            <Button className="mt-20 bg-[#f24c8e] text-[#f5f0e1] rounded-[30px] h-[83px] w-[392px] text-[28px] font-['Roboto_Slab-Regular',Helvetica] hover:bg-[#e03a7c]">
              BEKIJK MIJN CREATIES
            </Button>
          </div>
        </header>

        {/* Green Separator */}
        <div className="w-full h-[95px] bg-[#3cb371]"></div>

        {/* Portfolio Section */}
        <section className="py-16">
          <h2 className="font-['Roboto_Slab-Bold',Helvetica] font-bold text-[#ff8c00] text-6xl text-center mb-16">
            RECENT WORKS
          </h2>

          <div className="grid grid-cols-2 gap-6 px-[227px]">
            {portfolioProjects.map((project, index) => (
              <Card
                key={index}
                className={`w-full h-[525px] ${project.color} border-none rounded-none overflow-hidden`}
              >
                {project.image && (
                  <img
                    src={project.image}
                    alt="Portfolio project"
                    className="w-full h-full object-cover"
                  />
                )}
              </Card>
            ))}
          </div>

          <div className="mt-16 flex flex-col items-center">
            <p className="font-['Montserrat-Regular',Helvetica] font-normal text-black text-[25px] text-center max-w-[954px]">
              Hier vind je een aantal van mijn nieuwste ontwerpen. Stuk voor
              stuk werken waar kleur en duidelijkheid samenkomen om echt iets te
              vertellen. Neem gerust een kijkje!
            </p>
            <Button className="mt-10 bg-[#ff8c00] text-[#f5f0e1] rounded-[30px] h-[83px] w-[392px] text-[28px] font-['Roboto_Slab-Regular',Helvetica] hover:bg-[#e67e00]">
              BEKIJK MEER PROJECTEN
            </Button>
          </div>
        </section>

        {/* Contact Section */}
        <footer className="w-full bg-[#ff8c00] py-10">
          <div className="max-w-[1440px] mx-auto px-12">
            <div className="flex flex-col items-center md:items-start mb-12">
              <h2 className="font-['Roboto_Slab-Bold',Helvetica] font-bold text-white text-[40px] text-center mt-8">
                DINA VERCAMMEN
              </h2>
              <h3 className="font-['Roboto_Slab-Bold',Helvetica] font-bold text-white text-[40px] text-center mt-8">
                GRAPHIC DESIGNER
              </h3>

              <div className="mt-12 w-full max-w-[485px]">
                <Button
                  variant="secondary"
                  className="w-full h-[53px] rounded-[30px] bg-white text-[#ff8c00] text-[28px] font-['Roboto_Slab-Regular',Helvetica] mb-6"
                >
                  Dinavercammen13@outlook.com
                </Button>
                <Button
                  variant="secondary"
                  className="w-full h-[53px] rounded-[30px] bg-white text-[#ff8c00] text-[28px] font-['Roboto_Slab-Regular',Helvetica]"
                >
                  0499 74 41 60
                </Button>
              </div>
            </div>

            {/* Social Media Icons */}
            <div className="flex justify-center md:justify-start gap-6 mt-8">
              <Button
                variant="ghost"
                className="w-[90px] h-[90px] p-0 rounded-full"
              >
                <img
                  src="TIKTOK.png"
                  alt="TikTok"
                  className="w-full h-full object-cover"
                />
              </Button>
              <Button
                variant="ghost"
                className="w-[90px] h-[90px] p-0 rounded-full"
              >
                <Instagram size={90} className="text-white" />
              </Button>
              <Button
                variant="ghost"
                className="w-[90px] h-[90px] p-0 rounded-full"
              >
                <Linkedin size={90} className="text-white" />
              </Button>
            </div>
          </div>
        </footer>
      </div>
    </div>
  );
}
