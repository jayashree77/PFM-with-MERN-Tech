import mongoose from "mongoose";
import dotenv from "dotenv";

dotenv.config(); // Load environment variables from .env

export const connectDB = async () => {
  try {
    const dbURI = process.env.MONGO_URI || "mongodb://localhost:27017/expense"; // Default for local use
    const { connection } = await mongoose.connect(dbURI, {
      useNewUrlParser: true,
      useUnifiedTopology: true,
    });

    console.log(`MongoDB Connected to ${connection.host}`);
  } catch (error) {
    console.error("MongoDB connection error:", error);
    process.exit(1); // Exit process on failure
  }
};
