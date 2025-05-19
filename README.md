import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { motion } from "framer-motion";
import { Camera, Heart, Calendar } from "lucide-react";

export default function WeddingPhotographySite() {
  return (
    <div className="min-h-screen bg-white text-gray-800">
      <header className="bg-pink-50 py-10 px-6 text-center shadow-md">
        <h1 className="text-4xl font-bold text-pink-600">Chitralekha Wedding Photography</h1>
        <p className="text-lg mt-2">Capturing Love, One Frame at a Time</p>
      </header>

      <section className="p-8 grid grid-cols-1 md:grid-cols-3 gap-6">
        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-lg">
            <CardContent className="p-6 text-center">
              <Camera className="w-10 h-10 text-pink-500 mx-auto" />
              <h2 className="text-xl font-semibold mt-4">Our Style</h2>
              <p className="mt-2 text-gray-600">
                Timeless, candid, and elegant storytelling for your big day.
              </p>
            </CardContent>
          </Card>
        </motion.div>

        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-lg">
            <CardContent className="p-6 text-center">
              <Heart className="w-10 h-10 text-pink-500 mx-auto" />
              <h2 className="text-xl font-semibold mt-4">Love Stories</h2>
              <p className="mt-2 text-gray-600">
                Explore our portfolio of weddings captured across stunning locations.
              </p>
            </CardContent>
          </Card>
        </motion.div>

        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-lg">
            <CardContent className="p-6 text-center">
              <Calendar className="w-10 h-10 text-pink-500 mx-auto" />
              <h2 className="text-xl font-semibold mt-4">Book Now</h2>
              <p className="mt-2 text-gray-600">
                Secure your date and let’s create something magical together.
              </p>
              <a
                href="https://wa.me/919652246397"
                target="_blank"
                rel="noopener noreferrer"
              >
                <Button className="mt-4 bg-pink-500 hover:bg-pink-600 text-white">
                  Contact via WhatsApp
                </Button>
              </a>
            </CardContent>
          </Card>
        </motion.div>
      </section>

      <section className="p-8 max-w-3xl mx-auto">
        <h2 className="text-2xl font-bold text-center text-pink-600 mb-6">Inquiry Form</h2>
        <form
          className="grid gap-4"
          onSubmit={(e) => {
            e.preventDefault();
            window.open("https://wa.me/919652246397", "_blank");
          }}
        >
          <Input type="text" placeholder="Your Name" className="p-3 border rounded-xl" required />
          <Input type="email" placeholder="Your Email" className="p-3 border rounded-xl" required />
          <Input type="text" placeholder="Wedding Date" className="p-3 border rounded-xl" />
          <Textarea placeholder="Tell us about your wedding..." className="p-3 border rounded-xl" rows={4} />
          <Button type="submit" className="bg-pink-500 hover:bg-pink-600 text-white rounded-xl">Send via WhatsApp</Button>
        </form>
      </section>

      <footer className="text-center p-6 bg-pink-50 mt-10">
        <p>&copy; 2025 Chitralekha Wedding Photography. All rights reserved.</p>
      </footer>
    </div>
  );
}
